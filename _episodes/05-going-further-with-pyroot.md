---
title: "Using ROOT with python"
teaching: 0
exercises: 0
questions:
- "Can I call ROOT from python?"
objectives:
- "Find resources"
keypoints:
- "PyROOT is a complete interface to the ROOT libraries"
---

## PyROOT

The PyROOT project started with Wim Lavrijsen in the late `00s and became very popular, 
paralleling the rise of more general python tools within the community. Python has become the primary analysis language for the majority of HEP experimentalists. It has a
rich ecosystem that is constantly evolving. This is a good thing because it means that improvements
and new tools are always being developed, but it can sometimes be a challenge to keep up with the 
latest and greatest projects! :)

If you want to learn how to use PyROOT, you can go through some individual examples
[here](https://root.cern.ch/doc/master/group__tutorial__pyroot.html), or a more guided tutorial
[here](https://root.cern/manual/python/).

Feel free to challenge yourself to rewrite the previous C++ code using PyROOT!

## Using the Python docker container

The tools in the Python docker container will allow you to can easily open
and analyze ROOT files. This is useful for when you make use of the CMS open data tools to skim 
some subset of the open data and then copy it to your local laptop, desktop, or perhaps an 
HPC cluster at your home institution. 

If you completed the [Docker pre-exercises](https://cms-opendata-workshop.github.io/workshopwhepp-lesson-docker/) 
you should already have worked through 
[this episode](https://cms-opendata-workshop.github.io/workshopwhepp-lesson-docker/03-docker-for-cms-opendata/index.html), under **Download the docker images for ROOT and python tools and start container**, and you will have

- a working directory `cms_open_data_python` on your local computer
- a docker container with name `my_python` created with the working directory `cms_open_data_python` mounted into the `/code` directory of the container.

Start your python container with

~~~
docker start -i my_python
~~~
{: .language-bash}

In the container, you will be in the `/code` directory and it shares the files with your local `cms_open_data_python` directory.

If you want to test out the installation, from within Docker you can launch and 
interactive python session by typing `python` (in Docker) and then trying

~~~
import uproot
import awkward as ak
~~~
{: .language-python}

If you don't get any errors then congratulations! You have a working environment and you are ready to
perform some HEP analysis with your new python environment!


{% include links.md %}