---
title: "Write the code"
teaching: 30
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- How do you write the code that matches our physics selection criteria?
- Do we process collision data differently from our simulation data?
- How do we keep track of everything?
- What do we write out when we process a file?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Learn to use `awkward` arrays to select subsets of the data
- Understand how to apply the luminosity mask
- Make a first-order plot of some of our variables of interest
- Process at least one file of both simulation and collision data

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

There is a significant amount of code to run here and so we have written the majority of it in a Jupyter notebook. 
You can run most of the code on its own, but you should take the time to read and understand what is happening. 
In some places, you need to modify the code to get it to run. 

First, start your python docker container, following the lessons from 
[the pre-exercises](https://cms-opendata-workshop.github.io/workshop2024-lesson-docker/instructor/03-docker-for-cms-opendata.html). 
I am on a Linux machine, and I have already created the `cms_open_data_python` directory. So I will do the following

```bash
export workpath=$PWD
mkdir cms_open_data_python
chmod -R 777 cms_open_data_python
```

Start the container with

```bash
docker run -it --name my_python -P -p 8888:8888 -v ${workpath}/cms_open_data_python:/code gitlab-registry.cern.ch/cms-cloud/python-vnc:python3.10.5
```

You will get a container prompt similar this:

```output
cmsusr@4fa5ac484d6f:/code$
```

Before we start our Jupyter environment, let's download the notebook we'll be using with the following command. 

```bash
wget -O sdfsdfkjsdhfkdjshf
```

Now I will start Jupyter lab as follows. 

```bash
jupyter-lab --ip=0.0.0.0 --no-browser
```

and open the link that is printed out in the message.

:::::::::::::::: testimonial

## How to follow this lesson

While some of the code will be explained on this web page, the majority of the code
*and explanations of the code* are written out in the Jupyter notebook. Therefore, 
you should primarily following along there. 

I will use this webpage for the lesson to provide guideposts and checkpoints
that we can refer to as we work through the lesson.

:::::::::::::::::


## Running through the selection steps

### Preparing the environment

We will be making extensive use of the `uproot` and `awkward` python libraries 

### Read in some files

### Apply the cuts

Words

### Reconstruct the resonance candidate mass

Words

### Plot

Words


::::::::::::::::::::::::::::::::::::: keypoints 

- Use `.md` files for episodes when you want static content
- Use `.Rmd` files for episodes when you need to generate output
- Run `sandpaper::check_lesson()` to identify any issues with your lesson
- Run `sandpaper::build_lesson()` to preview your lesson locally

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
