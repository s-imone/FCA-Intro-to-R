---
title: Welcome
description: 'This is a template chapter.'
---

## Prelims

```yaml
type: NormalExercise 
lang: r
xp: 100 
skills: 1
key: 6d87677cfe   
```


Welcome to FCA Intro to R! In the following sections we're going to learn the basics to plot and manipulate maps in R. 

Since we are at it, we'll also learn some basic stuff about `data.table` syntax. It's just more fun than dataframes, and also a lot more efficient.

Try typing `?data.table` in your console to take a look at the package documentation.
Let's start by loading two libraries: `data.table` and `zoo`. To do that, you can use the function `library()`. Once the libraries are loaded, let's take a look at the documentation for `zoo`.

The `data.table` object `crime.dt` will already be loaded to the environment. We can start by having a look at some of its basic properties. Try using the function `names()` to print its column names to your screen.


`@instructions`
- Load the `data.table` and the `zoo` library
- Change names to lower case
- Print `crime.dt` column names to screen

`@hint`
- Try `library()`
- `?` followed by any R command will open the relevant documentation, provided the right libraries are loaded to your environment.
- Have you tried `?names()`?

`@pre_exercise_code`

```{r}
# Load datasets and packages here.
library(data.table)
library(zoo)
crime.dt <- get(load("crime_dt_wide.rda")) # object name: crime.dt
```


`@sample_code`

```{r}
# Set column names to lower case
# ...
# Take a look at the documentation for zoo
# ...
# Print crime.dt column names
# ...
```


`@solution`

```{r}
setnames(crime.dt, names(crime.dt), tolower(names(crime.dt)))

crime.dt[, month := month(year.month)]
crime.dt[, year := year(year.month)]
```


`@sct`

```{r}
# Update this to something more informative.
all(names(crime.dt)==tolower(names(crime.dt)))
# test_object("names(crime.dt)", incorrect_msg = "Something is wrong with the column names of `crime.dt`. Make sure they are all lower case!.")
       
crime.dt[, class(month)=="integer"]
crime.dt[, class(year)=="integer"]

success_msg("Well done! Let's try to do something that's actually useful now.")
```


`@possible_answers`


`@feedback`


