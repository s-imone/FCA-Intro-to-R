---
  title: "Welcome"
  description: "This is a template chapter."
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
- Take a look at the documentation for `zoo`
-

`@hint`
- Here is the hint for this setup problem. 
- It should get students 50% of the way to the correct answer.
- So don't provide the answer, but don't just reiterate the instructions.
- Typically one hint per instruction is a sensible amount.

`@pre_exercise_code`

```{r}
# Load datasets and packages here.
load("crime_dt_wide.rda") # object name: crime.dt
setnames(crime.dt, 
```

`@sample_code`

```{r}
# Your
# sample
# code
# should
# be
# ideally
# 10 lines or less,
# with a max
# of 16 lines.
```

`@solution`

```{r}
# Answer goes here
# Make sure to match the comments with your sample code
# to help students see the differences from solution
# to given.
```

`@sct`

```{r}
# Update this to something more informative.
success_msg("Some praise! Then reinforce a learning objective from the exercise.")
```
