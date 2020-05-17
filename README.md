Applied Research with R
============

This page contains a collection of R tutorials, developed at the University of Maastricht for Applied Research courses that use R. 

The goal is to organize relevant material into modular components, for more efficient design and maintenance of material, that can be used across courses, and that are accessible to students during and after their studies.

Below we list the relevant handouts/tutorials.

![](./pics/venlorlogo.PNG)



# R Basics

* [Getting started](tutorials/R_basics_1_getting_started.md) ([shorter version](tutorials/R_basics_1_getting_started_short.md))
* [Data and functions](tutorials/R_basics_2_data_and_functions.md) ([practise template](practise/R_basics_2_data_and_functions_practise.Rmd))

# Data mangling in the tidyverse

This is a set of tutorials designed to teach using the tidyverse functions for data cleaning, reshaping, visualizing etc.
The chapter numbers are relevant chapters from the excellent (and freely available) book ["R for Data Scientists" (R4DS)](http://r4ds.had.co.nz/)

| Tutorial | R4DS chapter(s) | Core packages / functions |
|----|---|---|
| [R Basics](inputs/Assignments-tutorial-1-sol.html) | 4 | (base R functions) |
| [Transforming Data]() | 5 | dplyr: filter, select, arrange, mutate | 
| [Summarizing Data]() | 5 | dplyr: group_by, summarize |
| [Visualizing Data]() | 3 & 7 | ggplot2  |
| [Reshaping data]() | 12 | tidyr: spread, gather |
| [Combining (merging) Data]() | 13 | dplyr: inner_join, left_join, etc. | 
| [Basic string (text) handling]() | 14 | readr: str_detect, str_extract etc., iconv |

# Statistical Analysis
| Tutorial | Core packages / functions |
|----|---|
| [Basic statistics](tutorials/simple_modeling.md) | stats: lm, aov, t.test |
| [Advanced statistics overview](tutorials/advanced_modeling.md) | stats: glm, lme4: lmer, glmer |
| [Generalized linear models](https://htmlpreview.github.io/?https://github.com/ccs-amsterdam/r-course-material/blob/master/tutorials/generalized_linear_models.html) | stats: glm, family, sjPlot: tab_model, plot_model |
| [Multilevel Models](https://htmlpreview.github.io/?https://github.com/ccs-amsterdam/r-course-material/blob/master/tutorials/multilevel_models.html) | lme4: lmer, glmer, sjPlot: tab_model, plot_model |


# Reference cards

Reference cards are great ways to help you discover new functions, and remember old ones.
Don't feel overwhelmed (even we don't use half of these functions).

General R Basics:

+ [https://cran.r-project.org/doc/contrib/Short-refcard.pdf](https://cran.r-project.org/doc/contrib/Short-refcard.pdf)
+ [https://www.stats.ox.ac.uk/~snijders/siena/Rrefcard.pdf](https://www.stats.ox.ac.uk/~snijders/siena/Rrefcard.pdf)
+ [http://www.u.arizona.edu/~kuchi/Courses/MAT167/Files/R-refcard.pdf](http://www.u.arizona.edu/~kuchi/Courses/MAT167/Files/R-refcard.pdf)
+ [http://www.i3s.unice.fr/~malapert/R/pdf/base-r.pdf](http://www.i3s.unice.fr/~malapert/R/pdf/base-r.pdf)

RStudio Guide:

+ [http://www.rstudio.com/wp-content/uploads/2016/01/rstudio-IDE-cheatsheet.pdf](http://www.rstudio.com/wp-content/uploads/2016/01/rstudio-IDE-cheatsheet.pdf)

_Resources_: [https://rstudio.com/resources/cheatsheets/](https://rstudio.com/resources/cheatsheets/)

# Where to ask?

+ Google
+ Stackoverflow community: [https://stackoverflow.com/](https://stackoverflow.com/)
