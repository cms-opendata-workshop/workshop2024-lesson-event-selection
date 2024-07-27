---
title: "The physics of our analysis"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What is the signal we are searching for?
- What are the backgrounds we need to concern ourselves with?
- How will we select the data?
- What is a "boosted jet"?
- What trigger(s) will we be using?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand what makes the signal "look" different from our backgrounds?
- How does this translate into how we record and measure particle interactions in CMS?

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

We're going to try to reproduce parts of a 2019 CMS study for resonant production of 
top-antitop pairs. The paper can be found [here](https://arxiv.org/pdf/1810.05905) and
hypothesizes a particle with specific properties referred to as $Z'$ which is
produced in our proton-proton collisions and then decays to a top-antitop pair. 

$p p \rightarrow Z' \rightarrow t\overline{t}$

The original analysis searched for the $Z'$ assuming a range of masses. In the interests
of time, we will conduct our search assuming a mass of 2000 GeV/$c^2$ for the $Z'$. The
Monte Carlo for this process can be found [here](https://opendata.cern.ch/record/75156).
It might be helpful 
[to review how to find data and how to understand these records](https://cms-opendata-workshop.github.io/workshop2024-lesson-dataset-scouting/instructor/index.html), 
if you have not done so prior to the workshop. 

## Selection criteria

Words

### Physics requirements 

Words

### Trigger

Words

### Luminosity masking

Words


::::::::::::::::::::::::::::::::::::: keypoints 

- Use `.md` files for episodes when you want static content
- Use `.Rmd` files for episodes when you need to generate output
- Run `sandpaper::check_lesson()` to identify any issues with your lesson
- Run `sandpaper::build_lesson()` to preview your lesson locally

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
