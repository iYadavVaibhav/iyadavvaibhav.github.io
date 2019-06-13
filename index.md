---
layout: default
---

Welcome to my blog! I'm a software engineer turned data analyst learing data science ;) , currently living in Delhi, India. 

---

### Articles

Some of the very basic how to guides as I learn through:
{% for post in site.posts %}
{% unless post.categories contains 'notes' %}
- [{{ post.title }}]({{ post.url }})
{% endunless %}
{% endfor %}

### Notes

Reference docs I prepared for personal learning:
{% for post in site.categories.notes %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}

### Kaggle

Amazing place for data science enthusiasts. If you are learning data science you can find kernels and data sets on [Kaggle](https://www.kaggle.com). Some of my work are:
- [Linear Regression in Machine Learning](https://www.kaggle.com/iyadavvaibhav/machine-learning-linear-regression)
- [Distribution Plots using Seaborn](https://www.kaggle.com/iyadavvaibhav/data-viz-distribution-plots)

Or you may see all my Kernels [here](https://www.kaggle.com/iyadavvaibhav/kernels).


### Tableau Public

Data Visualization has been my passion since I started my journey in Data and Analytics. You can find some of the dashboards I created in Tableau below:
- [Whatsapp Chat Analysis](https://public.tableau.com/profile/iyadavvaibhav#!/vizhome/WhatsappChatAnalysis/Allsheets) - It shows chats by gender, time of the day and how chats grew over the month.
- [Personal Trip Expense Report](https://public.tableau.com/profile/iyadavvaibhav#!/vizhome/WeekendExpenseDB/DB) - It shows the expense by categories.

Or click here to browse my [Tableau Public Profile](https://public.tableau.com/profile/iyadavvaibhav).


### Old Work
- [Easy Soft Sys](http://www.easysoftsys.com) - College days start up.
- [First Website](https://sites.google.com/site/vebs0205/) - Late 2009, I created my personal site using google sites.

You can also find me on [LinkedIn](https://in.linkedin.com/in/iyadavvaibhav), [Github](https://github.com/iYadavVaibhav/) and [Twitter](https://twitter.com/iYadavVaibhav/).

Thank you for visiting!
