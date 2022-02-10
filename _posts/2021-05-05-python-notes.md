---
layout: post
title: R Python Conda PIPs Venv RegEx
categories: notes python
last_modified_at: 2021-08-24 13:43:39
---

Python Notes:
- [Python Coding Kaggle](https://www.kaggle.com/iyadavvaibhav/python-notes)
- [Pandas Kaggle](https://www.kaggle.com/iyadavvaibhav/pandas-notes)
- [Flask](../flask-notes) - back end web framework micro
- [Pelican](../pelican-python-notes/) - Static Site Generator

## Python for Animation and Modelling:

VPython GlowScript
- can be used to create objects and animate them
- VPython makes it unusually easy to write programs that generate navigable real-time 3D animations.
- https://www.glowscript.org/docs/VPythonDocs/videos.html


Manim
- can animate equations and plots
- https://github.com/3b1b/manim
- https://www.youtube.com/watch?v=ENMyFGmq5OA

Sage
- Allows equation animations and plotting
- https://www.sagemath.org/download-mac.html

Povray
- The Persistence of Vision Raytracer is a high-quality, Free Software tool for creating stunning three-dimensional graphics. The source code is available for those wanting to do their own ports.
- http://www.povray.org/

ImageMagick
- Create, edit, compose, or convert digital images.
- It can resize, flip, mirror, rotate, distort, shear and transform images, adjust image colors, apply various special effects, or draw text, lines, polygons, ellipses and Bézier curves.

EdX
- https://learning.edx.org/course/course-v1:CornellX+ENGR2000X+1T2017/home




## Anaconda and Conda Notes with Jupyter and R Studio

**Anaconda** is toolkit for Data Science.
- it includes ds and ml libraries along with conda, and 
- other tools like jupyter, rstudio etc.

**Conda** is package manager and environment manager, like pip,
- it can install packages and 
- can manage envs 
- It is a CLI

**Anaconda Navigator** is GUI to use conda.

Conda Basic Commands:
- `conda config --set auto_activate_base false` disables autoload base
- `conda update conda` updates conda
- `conda install PACKAGENAME ` installs pkg to default/active env
- `conda update PACKAGENAME ` updated pkg
- `pip install pkg` aslo intalls to active env

Conda Env Commands:
- `conda create --name py35 python=3.5` created new env and installs py 3.5
- `conda activate py35` activates
- `conda list` lists all akgs installed ina ctive env.

**Jupyter** name comes from Julia, Python and R,
- formerly known as *IPython Notebook*
- it is pkg, same as flask
- `pip install jupyter` or it comes installed in Anaconda dist.
- `jupyter notebook` runs a server to server jupyter notebooks at http://localhost:8888/tree

**R and RStudio** are statistical language and IDE,
- `r` or `R` - R console in terminal
- `Rscript my.r` - executes file in terminal
- `Rscript -e "getwd()"` - executes cmd in terminal, can quickly install a library.
- `R CMD BATCH my.r` runs R script and saves output to `my.r.Rout`
- To make R Script executable like `./my.r` then:
  - set permission to 755
  - add correct `#!` to top of file

```r
#!/usr/bin/env Rscript
sayHello <- function(){
   print('hello')
}

sayHello()
```

## Regex Notes:

Remove single line comments // from code:
- `\/\/.*$\n` - Finds all single line comments starting with //.
  - `\/\/` - string has //
  - `.*` - then has anything after that
  - `$\n` - then matches next line as well.
- Check and Validate on [Regex101](https://regex101.com/)