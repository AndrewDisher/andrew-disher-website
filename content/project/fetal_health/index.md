---
author: Andrew Disher
categories:
- R
- Data Modeling
date: "2023-08-23"
draft: false
excerpt: Fitting a Multinomial Logistic Regression model in R.  
featured: false
layout: single-sidebar
links:
- icon: door-open
  icon_pack: fas
  name: R Markdown Notebook
  url: https://andrewdisher.github.io/multinomial-logistic-regression/
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/AndrewDisher/multinomial-logistic-regression
subtitle: ""
tags:
title: Classifying Fetal Health Conditions
---

### Project Goal

The goal of this project was to create a multinomial logistic regression model to predict whether there was 
cause for concern regarding the fetal health of a child in the mother’s womb. 

Cardiotocography is a technique used to monitor the fetal heartbeat, fetal movements, and the 
uterine contractions during pregnancy and labor. The machine used to perform the monitoring 
is called a cardiotocograph. The [data set](https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification) 
used in this study consists of a plethora 
of measurements produced by Cardiotocograms (CTGs), the machines used to perform 
Cardiotocography. The aim was to use these measurements as predictors in our model to 
accurately classify the health status of a child in the womb. 

### The Notebook

The the R Markdown document that details the process I took to complete this task
can be viewed by clicking on the notebook link at the top of this page. The code
can be found by clicking on the code link above as well. 

### What I Learned

I had many goals I wanted to achieve when I started this project, and they are outlined 
as such:

- Practice fitting the multinomial logistic regression model
- Practice balancing data sets via over/under-sampling class stratified observations
- Applying Principal Component Analysis (PCA) to a set of predictors/features
- Use visualizations and computed metrics to assess model fit
- Practice using the `box` package for explicit package and function dependencies (instead of using library() calls)

Some of these goals, such as using the incredible [`box package`](https://klmr.me/box/articles/box.html) 
and creating various visualizations are code related. I enjoy learning about and 
using new packages, or packages that are at least new to me. I have used `box` in
Shiny apps before, but it is relatively new to me when using it in a statistical
modelling notebook setting. I believe it adds just as much value to these R Markdown
notebooks as it does to Shiny apps, and using it to enforce clarity and reduce 
function namespace clashes is invaluable. I will continue to use it in every project
I work on. 

The other goals are mainly oriented towards using and interpreting more complex
statistical concepts. Logistic regression is a tried-and-true distribution based
statistical modelling technique and its multinomial extension is something that
opens up new possibilities. Often, when a categorical response variable has more
than two classes, modelers will merge classes to ensure binary logistic regression
is usable. This obscures some of the true relationships within the data, however. 
The multinomial extension preserves the original relationships within the data and 
offers greater insight. It is an invaluable statistical tool that I can now add
to my arsenal. 

Applying class balancing to a multinomial response variable, as well as using
Principal Components Analysis (PCA) in this setting was good practice for me as a 
data modeler. There are always trade-offs when using these techniques, and applying them
to the fetal health data set has reinforced my understanding of those trade offs. 









