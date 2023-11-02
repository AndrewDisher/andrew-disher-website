---
date: "2023-10-27"
draft: false
excerpt: Docker and Shiny are two incredible technologies. Let's explore some of the 
         ways we can use them together! First, I'll give you a (very) brief introduction
         to both Shiny and Docker, and let you know what you can expect from this series. 
subtitle: ""
title: Introduction
weight: 1
---

## What is Docker? 
---
>Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker's methodologies for shipping, testing, and deploying code, you can significantly reduce the delay between writing code and running it in production.
>
> --<cite>Docker Documentation</cite>

With that out of the way, let's translate what it means in a nutshell. Docker lets
you package up your code in an isolated way. If you're creating an application, you can
package your app code up, along with its dependencies, and deploy it anywhere you'd like. 
That means you can deploy containers on any host machine with any operating system you choose, 
without worrying about it functioning differently than how you intended it to. 
You can start any container or stop any without it affecting any of the hardware and software 
infrastructure you already have in place. 

In the context of this blog series, we'll be using it to deploy R Shiny applications
built using the R programming language. These types of applications primarily focus 
on communicating data related concepts using the vast ecosystem of R packages available 
on the[ Comprehensive R Archive Network (CRAN)](http://lib.stat.cmu.edu/R/CRAN/). 

## What is R Shiny?
---
[R Shiny](https://www.rstudio.com/products/shiny/) is a web application development framework
that allows R programmers to easily create web applications without needing to know anything 
about HTML, CSS, or JavaScript. This makes it ideal for individuals with a deep knowledge of
statistical concepts to create applications that convey the fundamental 
complexity of statistics and machine learning to a wide audience. 

However, R Shiny is very extensible too. It becomes much more powerful in the hands of someone
who has knowledge of web development tools like HTML and CSS. Therefore, it is invaluable
in the hands of both the beginner and the veteran. 

There are many great examples of Shiny applications available on the [Posit website](https://shiny.posit.co/r/gallery/#user-showcase) that 
have use cases ranging from [tools that teach statistical concepts](https://shiny.posit.co/r/gallery/education/didacting-modeling/), to others that 
display the results of a [statistical analysis of genomic data](https://shiny.posit.co/r/gallery/life-sciences/genome-browser/), 
to [some that identify real estate investment opportunities](https://shiny.posit.co/r/gallery/finance-banking/real-estate-investment/). 
The possibilities are endless. 

## What to Expect from this Series?
---
When you combine these two technologies, you get a powerful set of tools for communicating 
data of all kinds to large audiences. What data you communicate and the reason is up
to you to find out, but I will show you the process of how to achieve the end result
by walking you through this process with some applications of my own. 

Some will be relatively simple examples of how to do this with vanilla Shiny and others will be more complex examples
using other technology frameworks. I am a huge fan of the R Shiny app framework called
[rhino](https://appsilon.github.io/rhino/), which is developed by [Appsilon](https://appsilon.com/), so
I will certainly be showing a few examples of how to dockerize rhino shiny apps. 

There are also other shiny app frameworks, such as [Golem](https://thinkr-open.github.io/golem/)
and [Leprechaun](https://leprechaun.opifex.org/#/), but I have no experience
with those at the moment, so I will not be covering Docker with them for now (although, I may in the future).

## Is this Series for Me?
---
If you are only just learning about R Shiny, I'd try to get some more 
Shiny app projects under your belt first on your local machine. Some great resources
for learning Shiny include:

- [Mastering Shiny](https://mastering-shiny.org/) by Hadley Wickham
- [Feature Demos](https://shiny.posit.co/r/gallery/#feature-demos) on the Posit Website
- [Outstanding User Interfaces with Shiny](https://unleash-shiny.rinterface.com/) by Kenton Russel.

I can't stress enough how helpful it was for me to browse the Feature Demos. If 
you're stuck wondering if a certain feature exists in Shiny, chances are, it does! 
Plus, posit has done a good job showing you how to implement features in minimal
working examples. 

Mastering Shiny has just about everything you need. It does a great job easing the R 
programmer into Shiny, without introducing too much about HTML and CSS. This is what I used
when I first started learning Shiny. Please make sure you read about Shiny modules
from this book. They are very important, especially when your Shiny apps grow large. 
Personally, I use modules even in small projects because they help you organize 
your code and the app structure just makes more sense. 

Outstanding User Interfaces with Shiny throws you into the deep end, so to speak, regarding
the use of CSS and HTML. It even introduces SASS, a preprocessor scripting language for
CSS that makes writing CSS infinitely easier and more powerful. Sometimes SASS is overkill,
but it is very nice for large projects. Get used to CSS first!

However, If you have some experience building Shiny applications and are curious about the different ways to deploy them, 
then this article is definitely for you. I'll be assuming that you understand Shiny modules
and that you have experience with tracking your project dependencies with a package
such as [renv](https://rstudio.github.io/renv/articles/renv.html). I use renv in just
about all my projects and I believe it is the best way to manage dependencies for R
projects at the time this article has been written. 

## Let's Get Started Already!
---

And with that out of the way, let's start deploying some applications! The next article
will focus mainly on introducing the first app we'll be deploying and setting up an AWS EC2
instance to host it on.


