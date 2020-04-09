# Workshop: Introduction to R

- **Course: VSK1004 Applied Researcher**

- **Lianne Ippel (last version modified by C. Utrilla Guerrero)**

- **April 15, 2020**

### [The Final assignment(s) can be downloaded here](https://github.com/carlosug/AppliedRR/raw/master/inputs/Assignments-tutorial-1.docx)



![](./pics/venlorlogo.PNG)


## Introduction

The idea of this session is to provide an introduction to using the statistical computing package known as R. This includes how to read data into R, perform various calculation, obtain summary statistics for data and carry out simple analyses. You should read and work through the given notes and seek clarification and help when required from one of the staff in the course.

## What is R?

The command language for R is a computer programming language but the syntax is fairly straightforward and it has many built-in statistical functions. The language can be easily extended with user-written functions. R also has very good graphing facilities.

Source: [https://en.wikipedia.org/wiki/R_(programming_language)](https://en.wikipedia.org/wiki/R_(programming_language))


## Obtaining and installing R and Rstudio

R can be downloaded directly from CRAN: [https://cran.r-project.org/](https://cran.r-project.org/) afterwhich you can install Rstudio Desktop: [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/) (follow the instructions for installation).

Also find a more extensive R introduction here: <https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf>

R studio is an interface of R and using these exercises you will learn how to work with the R language. R studio has 4 panels: Script, Console, Environment, and a help/plot/packages. The script is a log that allows you to do analysis. The output of the script is sent to the console. The environment shows what R `knows' currently: it is an overview of what R has in memory. The final panel is more diverse: it can show you help documentation, or it can show you the graph you asked for, or it gives you plainly an overview of the files that are currently accessible to R.  

![](./pics/rstudio.png)

## Reference cards

Reference cards are great ways to help you discover new functions, and remember old ones.
Don't feel overwhelmed (even we don't use half of these functions).
The printed cheatsheets are yours to keep!


General R Basics:

+ [https://cran.r-project.org/doc/contrib/Short-refcard.pdf](https://cran.r-project.org/doc/contrib/Short-refcard.pdf)
+ [https://www.stats.ox.ac.uk/~snijders/siena/Rrefcard.pdf](https://www.stats.ox.ac.uk/~snijders/siena/Rrefcard.pdf)
+ [http://www.u.arizona.edu/~kuchi/Courses/MAT167/Files/R-refcard.pdf](http://www.u.arizona.edu/~kuchi/Courses/MAT167/Files/R-refcard.pdf)
+ [http://www.i3s.unice.fr/~malapert/R/pdf/base-r.pdf](http://www.i3s.unice.fr/~malapert/R/pdf/base-r.pdf)

RStudio Guide:

+ [http://www.rstudio.com/wp-content/uploads/2016/01/rstudio-IDE-cheatsheet.pdf](http://www.rstudio.com/wp-content/uploads/2016/01/rstudio-IDE-cheatsheet.pdf)

_Resources_: [https://rstudio.com/resources/cheatsheets/](https://rstudio.com/resources/cheatsheets/)

## Where to ask?

+ Google
+ Stackoverflow community: [https://stackoverflow.com/](https://stackoverflow.com/)


## Starting playing with R

First thing first, we need to make sure that we will remember the purpose of this script and when it was created. We do that using the `#` symbol, as follows:

```{r}
# author: Lianne Ippel (but please fill out your own name here)
# date: 15th April, 2020
# Description: this is my very first attempt at writing code, Hurray! 
```

Now that we know what is this, see hello to everybody! To execute this code, select/highlight the piece of code you want to run and either press `Ctrl Enter` or click `Run` in the upper right corner of the script. 


