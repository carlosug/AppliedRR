# Workshop: Introduction to R
Lianne Ippel (last version modified by C. Utrilla Guerrero)
April 15, 2020
Course: VSK1004 Applied Researcher



![](./pics/venlorlogo.PNG)


## Introduction

The idea of this session is to provide an introduction to using the statistical computing package known as R. This includes how to read data into R, perform various calculation, obtain summary statistics for data and carry out simple analyses. You should read and work through the given notes and seek clarification and help when required from one of the staff in the course.

## What is R?

The command language for R is a computer programming language but the syntax is fairly straightforward and it has many built-in statistical functions. The language can be easily extended with user-written functions. R also has very good graphing facilities.

Source: [https://en.wikipedia.org/wiki/R_(programming_language)](https://en.wikipedia.org/wiki/R_(programming_language))


## Obtaining and instaling R and Rstudio

R can be downloaded directly from CRAN: [https://cran.r-project.org/](https://cran.r-project.org/) afterwhich you can install Rstudio Desktop: [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/) (follow the instructions for installation).

Also find a more extensive R introduction here: <https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf>

R studio is an interface of R and using these exercises you will learn how to work with the R language. R studio has 4 panels: Script, Console, Environment, and a help/plot/packages. The script is a log that allows you to do analysis. The output of the script is sent to the console. The environment shows what R `knows' currently: it is an overview of what R has in memory. The final panel is more diverse: it can show you help documentation, or it can show you the graph you asked for, or it gives you plainly an overview of the files that are currently accessible to R.  

![](./pics/rstudio.png)

## Reference cards

General R Basics:

+ https://cran.r-project.org/doc/contrib/Short-refcard.pdf
+ https://www.stats.ox.ac.uk/~snijders/siena/Rrefcard.pdf
+ http://www.u.arizona.edu/~kuchi/Courses/MAT167/Files/R-refcard.pdf

RStudio Guide:

+ http://www.rstudio.com/wp-content/uploads/2016/01/rstudio-IDE-cheatsheet.pdf

_Resources_: https://rstudio.com/resources/cheatsheets/

## Where to ask?

+ Google
+ Stackoverflow community: https://stackoverflow.com/




## Starting playing with R

First thing first, we need to make sure that we will remember the purpose of this script and when it was created. We do that using the `#' symbol, as follows:

```{r}
# author: Lianne Ippel (but please fill out your own name here)
# date: 15th April, 2020
# Description: this is my very first attempt at writing code, Hurray! 
```

Now that we know what is this, see hello to everybody! To execute this code, select/highlight the piece of code you want to run and either press `Ctrl Enter` or click `Run` in the upper right corner of the script. 

### 1. Open a new script and print 'Hello World'. 


```{r hello world}

print('Hello World')
```


#### _Exercise 1_: Can you please use `print()` function to write _"I love you R"_?
```{r}

# insert code here #


```

Lets practice the basics. We can start by using R as calculator. 

### 2. Use R as a calculator 

```{r as a calculator}
# examples of how R can be used as a calculator - THE BASICS
1+1
3-1
2*2
18/5
3**2
1+2^2
exp(2)
log(2)
sqrt(16)
```

I provide some examples but you can of course try other things yourself. Simply write the equation, select the equation and run the code as before.

#### _Exercise 2_: Can you please say to R to return the square root of π number?

Hint: $\pi$ in r is `pi`.

```{r as a calculator example}
sqrt(pi)

```


Well, calculator is nice, but R can do many more things. Let go ahead!

### 3. Create an object - Variables

Now, we start with the creation of 'objects'. Objects in R are containers that can hold numbers, words, large complex model results, any digital thing you can think of. You tell R to create an object with the assignment sign  '<-' . 

```{r objects I }
# An object which holds a word
wordObject <- 'word'
# An object which holds a number
numberObject <- 10 # variable "numberObject" allocate the value 2
```

Objects that contain numerical values, can also be used for calculation. But operation of objects should be only between numerical.

#### _Exercise 3_: Can you please multiply `wordObject` x 2, what happens?

```{r objects II}
# calculating with objects 
result <- numberObject * 2
result
print(paste("The result is:",result))
```

#### _Exercise 4_: A right triangle has a side length (cm) `a` of 6 and side length `b` of 5. What is the hyphotenuse `h`? Use pythagorean theorem to retun the result.

```{r}
a = 6
b = 5
# we now from pytagoras h^2 = a^2 + b^2. Since we wanted to know h, then h = sqrt(a^2 + b^2)
h = sqrt(a^2+b^2)
h
```

We already discussed different data types during the lecture, so now let's try some of these data types. 


### 4. Data types

#### 4.1. Vectors

There are many data types used in R: Vectors, _Matrix, Array, Data frames, and List_. Each of these data types can be stored in an object. Actually, the objects we just created are single ~~entree~~ vectors! Vectors can contain either number or strings (letters/words), but if you combine them, R will treat everything as string, meaning you can no longer use the ~~entrees~~ for calculation. 

When you want to select an entry from a vector, you do that as follows.  
```{r data vectors I}
# creating our first vector. Create a variable with 3 elements
firstVector <- c(1,2,3)
```

How would you access the second _element_ of *firstvector*?

To access an element of a vector use square brackets, _e.g_ elements number 2:

```{r data vectors II}
firstVector[2]
```

To access a series of elements, say from 1 to 3:

```{r data vector III}
firstVector[c(1:3)]
```


Say you want to change one particular entry, you do it as follows: 
```{r data vectors IV}
# creating our first vector 

firstVector[1] <- 7

# or if you want to include more numbers
firstVector <- c(firstVector, 8) # adding 8 to last element

#maybe include a missing number, 

firstVector <- c(firstVector , NA) #NA means Not Available/applicable  
``` 

##### _Exercise 5_: Can you please create a vector `b` with all prime number below 10, and another vector `b` that includes the last five letters of the latin alphabet?
(Hint: 2,3,5, [..])

```{r}
b <- c(2,3,5,7,11,13,17,19,23,29)
d <- c('V','W','X','Y','Z')
```

##### _Exercise 6_: Given the ten first natural numbers, find out:
  
+ 6th component _(Hint: To extract the sixth component of a vector we use square brackets)_.
+ Components in between 2sd - 9th both inclusive.
+ Components in between 2sd - 7th both inclusive, but highest to lowest
+ Convert last component into number 4
+ Calculate sum, mean, median and mode of these numbers

```{r}
x = (1:10)
x[6]
seq(2,9)
seq(9,2)
x[10] = 4
sum(x)
mean(x)
median(x)
table(x) # mode
```


#### 4.2. Matrix

The second data type, matrix, is very similar to a vector, with the only difference that a matrix has **rows and columns** 
```{r data matrices}
# creating our first matrix 

firstMatrix <- matrix(data = c(1,2,3), nrow = 6, ncol = 2)
firstMatrix

#select a row:
firstMatrix[1, ]
#select a column
firstMatrix[, 1]
#select a cell
firstMatrix[1,1]
```

Let us define a variable

```{r data matrices II}
z <- c(1,2,3,4)

```
using the function c() that combines its argument into a vector. The variable z is still numeric but

```{r matrices III}
z <- as.matrix(z)
```

Transform z to a matrix object and gives it new attributes such as dimensions
```{r matrices IV}
dim(z)
```

We can also reshape z to square matrix
```{r matrices V}
z <- matrix(z, ncol=2, nrow = 2)
```

which is the same as 
```{r matrices VI}
z <- matrix(c(1,2,3,4), ncol = 2, nrow = 2)
```

To select the cell in row 1 and column 2 type
```{r matrices VII}
z[1,2]
```

As you see right now, many vectors put in rows or column can make a matrix. The combination of the vector `a` and `b` that we previously created will generate a matrix. Use the following functions:

```{r}
cbind(b,d)
rbind(b,d)
```

##### _Exercise 7_: What is the difference between cbind() and rbind()? Explore the operations between matrices or vector and a matrix.

```{r}
# Intert here the answer
```

##### _Exercise 8_: Given matrix 2X3 in which the rows are the first six odd numbers consecutively, we ask:
- Convert to zero the element (2,3)
- Convert the matrix into a new one with 1x6 format
- Multiply the matrix x 6

```{r}
A = matrix(c(1,3,5,7,9,11), 2,3, byrow = TRUE)
A[2,3] = 0
A = matrix(c(1,3,5,7,9,11), 1,6)
A*6
```


An important takehome for different classes of objects is that different classes may have different methods defined for them (plotting a vector may be completely different from plotting, say, the regression output)

Please bare in mind that if you provided less data than there are spots available in the matrix (see example), that R will repeat the number, WITHOUT TELLING YOU! This is true for all data types, not just matrices. 

#### 4.3. Data frames

For your current research project, the data frame will be most important. Data frame looks very similar to a matrix, however, data frames can have both numerical and string data, without R converting everyting to strings. Just to speed things up a little, I am throwing in some additional function of R, which will be explained below:

```{r data frames}
# creating our first data frame  
help("data.frame")
firstDF <- data.frame(id = 1:10, gender = rep(c('male','female'), times = 5),
                      income  = rnorm(10, mean = 1500, sd = 50 ))
firstDF

#select a row:
firstDF[1, ]
#select a column
firstDF[, 1]
#or 
firstDF$gender
#select a cell
firstDF[1, 1]
#or
firstDF$id[1]

#want to add a variable?
firstDF$discipline <- rep(1:5, each = 2)
#need value labels?
firstDF$discipline <- factor(firstDF$discipline, levels = 1:5,
                             labels = c("Medicine", "Agtech",
                                        "Food", "Data science", NA))

```


##### _Exercise 9_: Delete the last column of the `firstDF` data frame.
```{r}
firstDF$discipline <- NULL

```


### 5. R functions 

Quick introduction to `rep()`. R has a lot of basic functions implemented. For instance if you want to repeat the same serie of numbers or strings.
Not sure on what you have to fill out after a command? type in your console: `?rep` 
This will activate the help window and give you information about how the rep command works. This works the same for every command in R. 
```{r new functions}
# repeat a set with multiple entries, numerical or string using rep() 
# check out the difference between these two options

rep(c(1,2), times = 5) # repeat the whole vector each ==5 times
rep(c(1,2), each = 5) # each element is repeated each == 5 times

```

#### _Question 10_: What is the difference between `each` and `times`?

```{r}
# Insert here your answer
```



### 6. Data Simulation

In need of practice data? You can create data yourself using `rnorm()`this command creates random data that follows a normal distribution with a mean and a  stddev. Now because this is random data, you will not get the exact same result.

```{r}
myData <- rnorm(n = 1000, mean = 5, sd = 1)
```


One way to force R to always give the same random sequence of numbers is by setting the seed:

```{r}
set.seed(98743) # choose a nice funny number
rnorm(n=5, mean = 0, sd = 1)
```


We can also use R to visualize our data, for instance by using a histogram: 


```{r}
hist(myData)
```


Write a function to compute the mean of 2 numbers, and add 1 to the mean. Below you see an example with default values, this is good practice but you have to be careful with defaults! 
```{r Functions }
meanPlus1 <- function(x1, x2, add = 1){ 
			average <- (x1 + x2) / 2
			result <- average + add
			return(result)} 

meanPlus1(1,2)
```

#### _Bonus Exercise_: Challenge code: 'Opposite number'


Very simple, given a number, find its opposite.
Examples:

Input     | Output
--------- | ---------
`1`       | -1
`24`      | -24
`33`      | 33


_Source_: [https://www.codewars.com/collections/learning-r](https://www.codewars.com/collections/learning-r)

```{r reverse Strings}
opposite <- function(number){
  ## your code here
  result = -number
  return(result)
}
number=1
opposite(number)
```


### 8. R Packages
Sometimes, the integrated functions of R are not exactly what you are looking for. In that case, you can check whether someone else has written it for you and made the code available. To include such a chunk of code, we have to install a 'package'. A google search will usually tell you which package you need. Say you want to read in Excel file, you can use the `readxl` package. If you want to read in an SPSS data file, use the foreign package.

```{r packages}
# usually we install packages via the console and attach them using the script, 
# can you imagine why?
# install.packages('readxl')
library(readxl)
# to read in a file use the following command 
# (but remove the #, and insert correct name of the file)
# myExcelData <- read_excel('name_of_the_file.xls') 
```


## Working with data

Lastly, R is only learned by doing it! Google is your friend --The most effcient avenue to help is to simply google whatever it is you want to do. I will finish this exercise by pointing you to some data that you can play with for the remaining time with some functions to learn the data a little better. You can select a dataset from the list that you get once you run the command: data(). For now let's look at mtcars.

Try finding some information about this data set. (hint: ?how do you ask for help in R). You can look at the spreadsheet of the data by using View(mtcars). Please mind that View is with a capital. Try plotting some variables. You can use hist(), or plot(), even boxplot works or google for some other kind of plot. Select a variable (see previously for the data frame, selecting a column) and compute the mean.  What do you see when you do table(mtcars$gear) , and what summary(mtcars\$carb) do? 

```{r}
sessionInfo()
traindf <- mtcars # import dataset
summary(mtcars)
```
How many cases and variables are there?
```{r}
dim(traindf)
```



We can also get an editable spread-sheet version of the data using function 'fix()':
```{r}
# fix(traindf)
```

#### _Exercise 11_: What summary measures can we give for the variable 'gear'? We can calculate the absolute numbers per category:

```{r}
table(traindf$gear)
```

Add new variable to give information about brand ('brandA', 'brandB'):

```{r}
traindf$brand <- rep(c('brandA','BrandB'))
```

To calculate the proportion of brands, we can take the mean of a Boolean that is equal to TRUE if a respondent is brandA

```{r}
mean(traindf$brand=='brandA')
```
The variable 'brand' is not numeric, so adding, substracting values for this variable does not make sense. To see what type of values a variable takes type:

```{r}
mode(traindf$brand)
```

#### _Exercise 12_: What is the average units of 'wt'?

(Hint: We can do it "manualy" using the definition of the arithmetic mean or using the build function 'mean'. Firt manually, $x_{1}$ + $x_{2}$ + . + $x_{n}$ and divide the result by the number of _n_.)

```{r}
N = nrow(traindf)
sum(traindf$wt) / N
```

#### _Exercise 13_: What about using the function?

```{r}
mean(traindf$wt)
```

#### _Exercise 14_: Is the median greater or smaller than the mean and does it mean that the distribution is skewed?

```{r}
median(traindf$wt)
```


Now we continue with some other measures. To get a sense of the variation calculate the minimun and maximun values and the variance
```{r}
range(traindf$wt) # This will give same results as calculating min and max
```


As for the mean we are going to calculate the variance manually first. The expression 
$\sigma^{2}$ = $\frac{\sum((x - \bar{x})^{2})}{-1}$ written is R is:

```{r}
sum((traindf$wt - mean(traindf$wt))^2)/(N-1)
```
and the built function is:
```{r}
var(traindf$wt)
```

#### _Exercise 15_: To get a visual confirmation of your summary measures of _wt_, draw a histogram please.

```{r}
hist(traindf$wt)
```

#### _Exercise 16_: Visualise the distribution of _brand_ in the data.

Note that neither 'plot()' nor 'hist()' works with _traindf$brand_ as the values are nonnumerical. 

We use 'table()' again, to provide the plotting function the frequencies.
```{r}
barplot(table(traindf$brand))
```

### 9. Lastly some bivariate summaries


Plotting _wt_ against _brand_ is not particularly instructive. We can however make a histogram of _wt_ only for brandA

```{r}
hist(traindf$wt[traindf$brand=='brandA'])
```

To investigate whether the _wt_ differs between brands, you can calculate group-wise means as:

```{r}
aggregate(traindf$wt, by = list(traindf$brand), mean)
```

We can cross-tabulate choice of brands and wt easily using the function 'table' as above.We can get a grouped bar-chart by applying 'barplot()' to the table:

```{r}
barplot(table(traindf$wt, traindf$brand))
```

### 10. Bonus: Experiment on Plan Growth.

A research group compared yields (as measured by dried weight of plans) obtained under a control and two different treatment conditions.

+ Data Format: A data frame of 30 cases on 2 variables.

To import data into R please run following code:

```{r}
data("PlantGrowth")
?PlantGrowth
str("PlantGrowth")
View(PlantGrowth)
```


[, 1]	weight	numeric
[, 2]	group	factor
The levels of group are ‘ctrl’, ‘trt1’, and ‘trt2’.

_Source: Dobson, A. J. (1983) An Introduction to Statistical Modelling. London: Chapman and Hall._

#### _Exercise BONUS_: Can you perform a very brief descriptive statistics summary?

* there is no right or wrong in the assignment*

