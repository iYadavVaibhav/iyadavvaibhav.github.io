---
layout: post
title: How to setup Github Pages and Jekyll Sites
categories: howtos
---

Github Pages are static sites that can be hosted on GitHub for free. Github Pages use Jekyll (a Ruby Gem) to build static site from markdown files.

## Quickest way to get started

Use 'Jekyll Now', it is flat 30 seconds blog setup. Follow the steps below:
- You can setup Jekyll on GitHub by forking [Jekyll Now](https://github.com/barryclark/jekyll-now) repository.
- The readme.md in above repository is a very good tutorial that you can follow and setup Jekyll on your GitHub account.
- Modify config files and github settings as stated in above readme.
- your blog is live

With this you can use your time on writing post rather than other geeky stuff, but if you need to setup everything or if it is required your can follow setting Jekyll locally below.

Now that blog is working, we need to write posts.

## Publishing Posts
Posts can be published in 3 ways:

1. Directly write on GitHub.com:
This is fastest way and requires no setup. You can go to `_posts` folder on this repository and create new .md file.

2. Local MD files
You can use Sublime, atom or any other text editor on your local machine and the upload it to GitHub or use Git locally then commit and push to GitHub.

3. Local Jekyll setup
You can install Jekyll locally on your machine. This will require you to install Ruby as well. Then on localhost you can render your entire website (blog) and see changes. Then you can push it to GitHub.

## Setting up Jekyll locally:
- You need to have ruby, gem, gcc and g++ installed. else do `brew install gem` and all.
- Then you need to install `gem install bundler jekyll`
- Next, `gem install github-pages` installs all gems required by github pages, all of the dependancies you’ll need, like: kramdown, jemoji, and jekyll-sitemap
- `jekyll new my_blog` creates scaffold for a new site. This is all you need to do.
- `jekyll build` builds
- `jekyll serve` serves the site to localhost:4000.
- Detailed article can be found [here](https://jekyllrb.com/docs/installation/).
- Advanced features: If you need to extend the functionality of Jekyll posts then advanced tutorial can be found at [here](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/).

Issues:
- If you see permission issue on Mac, run using `sudo`. This may occur as gem and ruby are already installed on mac but in Library folder which is not writable.
- If you want to run locally already **existing site**, then create a new temp blog then copy 'Gemfile' and 'Gemfile.lock'. The site root should have these files. They are required to provide all gems that Jekyll requires for proper functionality.

## Extending Sublime Text for Markdown Support:
If you want more syntax highlighting and better preview of what you write then you can extend Sublime Text by installing  package, follow steps below:
- Type: ``Cmd + Shift + P`` to open package manager.
- Then type ``install package`` and hit enter. This will provide you list of available packages from packagecontrol.io
- Next when you get dropdown type ``Markdown`` and this will list you all markdown related packages.
- You can select ``Markdown Editing`` to install the package. This provides much better highlighting and preview.

I, personally, didn't like it much and was a bit distracting for me. So I removed this package. But you may like it. 

Removing a package from Sublime Text:
- press ``Cmd + Shift + P`` and 
- then type ``remove package``. This will give you list of packages installed and 
- next select ``Markdown Editing`` to remove it.

Recently VS Code turned out to be best editor for Markdown however it is bit heavy. Also 'Markdown Preview' extension on Chrome makes it handy to preview markdown files.

## Github Site for Projects
Github can further be used to host your projects site. This is kind of a sub-site/sub-domain of main site.

My site:
```myname.github.io/```

Project Site:
```myname.github.io/abc_project/```

All projects repository come under **gh-pages** branch and not master.

Creating a sub site is same as creating a main site.

## Related post:
- [How to add syntax highlighting to Jekyll Sites](../syntax-highlight-jekyll)
