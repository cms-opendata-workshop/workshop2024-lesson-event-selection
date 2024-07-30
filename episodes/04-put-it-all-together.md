---
title: "Putting it all together"
teaching: 20
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- Do we process collision data differently from our simulation data?
- How might we process multiple files? 

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Run over multiple collision or simulation files
- Develop a sense of how long it takes to run over lots of data and how you might scale it up

::::::::::::::::::::::::::::::::::::::::::::::::

# Introduction

We're going to continue to work with the same Jupyter notebook as before, picking up
exactly where we left off with the **Processing data files** section. 

## Processing data

Follow the notebook to develop a sense of how we apply the luminosity masking, following
the concepts introduced in a [previous lesson](https://cms-opendata-workshop.github.io/workshop2024-lesson-triggers-lumi/instructor/index.html).

## Processing multiple files

The notebook has an example of how all of the previous cuts and data processing can be put into 
one function that is easily called. 

You can return the data in any format you like, but we chose to use [pandas DataFrame objects](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html).
They are widely used in many data science communities and can make simple data analysis much easier. 

Make sure you get through the examples so that you have processed at least a few files from different
datasets. 

:::::::::::::::: testimonial

## How much data should I run over?

It can take 6-12 hours to run over all the data for this lesson, depending on your computer's speed and
your internet connection. 

We recommend that for this lesson you do *not* process all the data yourself. For future lessons, we will have processed all the
data for you. 

:::::::::::::::: 

:::::::::::::::: challenge
# Activity!

Once you are able to run over multiple files, try to make some additional plots, either from the dataframes
or from the earlier code where you are processing things step-by-step. 

Try making some plots to compare the signal with one of the background samples. Are they different? Similar? 

Are either of them similar to the collision data? 

Add your plots to the Google document listed in the Mattermost channel for this lesson. 

:::::::::::::::: 

::::::::::::::::::::::::::::::::::::: keypoints 

- It it up to you how you want to save your reduced data and how to keep track of everything
- There are many options, but think about how you might scale things up

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
