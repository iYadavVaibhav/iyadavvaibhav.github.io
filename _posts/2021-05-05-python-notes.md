---
layout: post
title: Python Conda PIPs Venv RegEx R
categories: notes python
last_modified_at: 2021-08-24 13:43:39
---

## Other Python Notes

- [Python Coding Kaggle](https://www.kaggle.com/iyadavvaibhav/python-notes)
- [Pandas Kaggle](https://www.kaggle.com/iyadavvaibhav/pandas-notes)
- [Flask](../flask-notes) - back end web framework micro
- [Pelican](../pelican-python-notes/) - Static Site Generator

## Web Scraping - Selenium

Install web driver

- visit `https://chromedriver.chromium.org/downloads` and download version same as your browser version.
- unzip and move `chromedriver` to `/usr/local/bin/chromedriver`

More - <https://realpython.com/modern-web-automation-with-python-and-selenium/>



## Data Science Setup

Python installed in Ubuntu or Mac should not be used. Instead create a Virtual Environment for it.

**Virtual Environments** can be created using conda or venv module. Each virtual environment has its own Python binary and can have its own independent set of installed Python packages in its site directories. More [here](https://docs.python.org/3/library/venv.html).

**Quick Start on Linux** more [here](https://cloud.google.com/python/docs/setup).

```sh
sudo apt update
sudo apt install python3 python3-dev python3-venv

sudo apt-get install wget
wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py

pip --version

cd your-project
python3 -m venv env

source env/bin/activate
```

This will create a dir `env` and will have its own python, python3, pip and pip3. Now you can install any packages and this will not interfere with system.



**Conda** is package and virtual environment manager, like pip, for any language—Python, R, Ruby and more. It is a CLI and can

- install packages like flask, jupyter, pandas etc.
- can manage envs, virtual environment is separate python and its packages. This means each project you work on can have its own set of packages.

**Anaconda** is toolkit for Data Science. Along with conda it includes ds and ml libraries (500Mb) installed.

**Anaconda Navigator** is GUI to use conda.

**Miniconda** includes conda and python but not much libraries.

So we can use conda alone to create a development virtual environment for new data science project or use miniconda.

**Installing Conda** on Linux

- `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
- `bash Miniconda3-latest-Linux-x86_64.sh` this installs python, conda, vevn and others, all in virtual environment.
- After installation, restart terminal, and it will load new environmnet called 'base'. Now python is not the default system python.
  - If you'd prefer that conda's base environment not be activated on startup, set the auto_activate_base parameter to false: `conda config --set auto_activate_base false`
  - more: <https://www.projectdatascience.com/step-by-step-guide-to-setting-up-a-professional-data-science-environment-on-a-linux/>

**Quick Start using Conda** for a new project

```sh
conda deactivate
mkdir prj1
cd prj1
conda create -n prj1env pandas numpy jupyter scikit-learn matplotlib seaborn
conda activate prj1env
touch README.md
code .
```

Run `conda activate prj1env` in code shell.

Undo `conda deactivate && conda remove --name prj1env --all` and remove files if any.

**Install Jupyter** in the venv. Now that we have an environment (base) you can use it, or create a new. Then

- `pip install jupyter`
- `which jupyter` shows `/home/vaibhav/code/miniconda3/bin/jupyter` it does not effect the system python.

**Conda Basic Commands**

- `conda update conda` updates conda
- `conda install PACKAGENAME` installs pkg to default/active env
- `conda update PACKAGENAME` updated pkg
- `pip install pkg` aslo intalls to active env

**Conda Env Commands**

- `conda create --name py35 python=3.5` created new env called 'py35' and installs py 3.5
- `conda activate py35` activates
- `conda list` lists all packages installed in active env.
- `conda remove --name my-env --all` deletes the env.

**Jupyter** name comes from Julia, Python and R,

- formerly known as *IPython Notebook*
- it is pkg, same as flask
- `pip install jupyter` or it comes installed in Anaconda dist.
- `jupyter notebook` runs a server to server jupyter notebooks at <http://localhost:8888/tree>

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

## Regex Notes

Remove single line comments // from code:

- `\/\/.*$\n` - Finds all single line comments starting with //.
  - `\/\/` - string has //
  - `.*` - then has anything after that
  - `$\n` - then matches next line as well.
- Check and Validate on [Regex101](https://regex101.com/)

## Python for Animation and Modelling

VPython GlowScript

- can be used to create objects and animate them
- VPython makes it unusually easy to write programs that generate navigable real-time 3D animations.
- <https://www.glowscript.org/docs/VPythonDocs/videos.html>


Manim

- can animate equations and plots
- <https://github.com/3b1b/manim>
- <https://www.youtube.com/watch?v=ENMyFGmq5OA>

Sage

- Allows equation animations and plotting
- <https://www.sagemath.org/download-mac.html>

Povray

- The Persistence of Vision Raytracer is a high-quality, Free Software tool for creating stunning three-dimensional graphics. The source code is available for those wanting to do their own ports.
- <http://www.povray.org/>

ImageMagick

- Create, edit, compose, or convert digital images.
- It can resize, flip, mirror, rotate, distort, shear and transform images, adjust image colors, apply various special effects, or draw text, lines, polygons, ellipses and Bézier curves.

EdX

- <https://learning.edx.org/course/course-v1:CornellX+ENGR2000X+1T2017/home>

