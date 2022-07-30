---
title: Tableau Notes
categories: notes
last_modified_at: 2022-07-31 12:42:21
---

Tableau is a data analysis and visualization tool.

## Date Calculations

Here are some basic common calculations that helo in making **KPIs** and easy working with dates to find YOYs and MOMs

- Month-Year to Business Date `DATEPARSE('yyyy-MM-dd',[Business Month]+'-01')`
- Month-Year to Business Year - `Left([Business Month],4)`
- Max Date - `{MAX([Business Date])}`

- Monthly

```javascript
IF ( DATEDIFF('month', [Business Date], [Max Date], 'monday') = 0  AND DAY([Business Date])<=DAY([Max Date]))
THEN 'Current Month'
ELSEIF ( 
    DATEDIFF('month', [Business Date], [Max Date], 'monday') = 1
    //AND
    //DAY([Business Date])<=DAY([Max Date])
)
THEN 'Last Month'
ELSEIF ( 
    DATEDIFF('month', [Business Date], [Max Date], 'monday') = 12 
    // AND DAY([Business Date])<=DAY([Max Date])
)
THEN 'Last Year Month'
END
```

- Rolling 13 months

```javascript
[Business Date] > DATEADD('month',-13,{MAX([Business Date])})
and
[Business Date] <= {MAX([Business Date])}
```

- yearly

```javascript
IF ( DATEDIFF('year', [Business Date], [Max Date], 'monday') = 0   AND MONTH([Business Date])<=MONTH([Max Date]))
THEN 'Current Year'
ELSEIF ( 
    DATEDIFF('year', [Business Date], [Max Date], 'monday') = 1  
    AND ( 
            (  MONTH([Business Date]) <= MONTH([Max Date])  ) 
            //OR 
            //( 
                // ( MONTH([Business Date])=MONTH([Max Date]) ) AND ( DAY([Business Date])<=DAY([Max Date]) ) 
            //)
        )
)
THEN 'Last Year'
END
```

- CM `SUM(IIF([Monthly]=='Current Month',[Closed Customers],NULL))`

- MOM

```javascript
(
    SUM(IIF ([Monthly] == 'Current Month',[Users],0)) - 
    SUM(IIF ([Monthly] == 'Last Month',[Users],0) ) 
)
/
SUM(IIF ([Monthly] == 'Last Month',[Users],0))
```

- MOM up `IF [Closed Customers MOM] > 0 THEN "▲" END`
- MOM Donw `IF [Closed Customers MOM] <= 0 THEN "▼" END`

- YOY

```javascript
( SUM(IIF ([Yearly] == 'Current Year',[Closed Customers],0)) - SUM(IIF ([Yearly] == 'Last Year',[Closed Customers],0) ) )
/
SUM(IIF ([Yearly] == 'Last Year',[Closed Customers],0))
```

- YOY Up `IF [Closed Customers YOY] > 0 THEN "▲" END`
- YOY Donw `IF [Closed Customers YOY] <= 0 THEN "▼" END`
- YTD `SUM(IIF([Yearly] == 'Current Year',[Closed Customers],0))`

**KPI Format**

- small arrows `0%  ⯅; -0% ⯆; 0%⠀⠀;` ⯇ ⯈ ⯅ ⯆
- ⮜ ⮞ ⮝ ⮟ `0%  ⮝; -0% ⮟; 0%⠀⠀;`  \(U+2800\)
- 🡄 🡆 🡅 🡇 `0%  🡅; -0% 🡇; 0%⠀⠀;`
- more arrows - <http://xahlee.info/comp/unicode_arrows.html>

TUG Austia - <https://github.com/tableau/community-tableau-server-insights> - readymade events

**Number Tweaks**

Number standardize between 0 and 1 per category for trend line colors

```javascript
(
    SUM([Value ]) - WINDOW_MIN(SUM([Value ])) 
)
 /
(
    WINDOW_MAX(SUM([Value ])) - WINDOW_MIN(SUM([Value ])) 
)
```

## Links

- Data Structuring for Analysis - <https://help.tableau.com/current/pro/desktop/en-us/data_structure_for_analysis.htm>
