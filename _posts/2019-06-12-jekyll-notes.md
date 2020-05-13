---
layout: post
categories: notes
title: Understanding Jekyll
---

Jekyll is a Ruby library to make blog and pages site.

**_config.yml** has all configuration variables.

**Posts** are markdown files store under \_posts folder

**Pages** are markdown files in root location.

**_layouts** have different .html files that define the layout for example: default, pages or posts. These can include other templates from **_includes** folder. They have `{{ content }}` which gets populated by file that uses this layout. 

For eg. 'default.html' can include 'meta.html'.

'post.html' can use 'default.html' as layout. So all code in 'post.html' will populate `{{ content }}` in default.html

**some_post.md** can use `post.html` as layout. So all markdown from this file will be populated to `{{ content }}` of 'post.html'.

**To list all categories in site**

Category returns two array items, first is category name and second is another array of posts.

Categories in site:
```ruby
{\% for category in site.categories \%}
- {{ category[0] }}
{\% endfor \%}
```

