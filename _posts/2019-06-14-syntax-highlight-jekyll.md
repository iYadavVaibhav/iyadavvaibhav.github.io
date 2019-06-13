---
layout: post
title: How to add syntax highlighting to Jekyll Sites
categories: howtos
---

Jekyll supports syntax highlighting by default using gem `rouge`.

Ruby:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

Python:

```python
import numpy as np
import pandas as pd

df = pd.read_csv('employee.csv')

df.head()
```

HTML

```html
<head>
  <body>
    Hello..!
  </body>
</html>
```
