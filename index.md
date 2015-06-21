---
title       : Developing Data Products Project
subtitle    : BMI Calculator
author      : Sanya B
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

The BMI Calculator appication is designed as part of Coursera's Developing Data Products Course Project. This course is a part of the Data Science Specialization track. The application takes as input height and weight of the user, calculates the BMI (Body Mass Index) of the person and prints it out.

The application includes the following:
- Numeric input fields to enter height in feet and inches and weight in kgs.
- Minimum and maximum values of each input field have been set.
- Default values displayed on load of the application.
- Operation performed on the ui input in server.R
- BMI computed and displayed as a result of server calculations

--- .class #id 

## BMI Calculation

The Body Mass Index is calculated as follows:   

Weight (in kgs) / (Height (in m) x Height (in m))

- The application accepts the weight in kg and height in feet and inches and performs the necessary conversion of units as per the formula.

--- .class #id 

## BMI Calculation in R

Suppose, I weigh 55 kgs and I am 5 feet and 5 inches tall, the BMI shiny app would calculate my Body Mass Index in the following manner.



```r
feet=5
inch=5
kg=55

bmi=kg/((((feet*12)+inch)*0.025)^2)
print(bmi)
```

```
## [1] 20.8284
```

BMI formula requires the height to be in metres if the weight is in kgs, hence we multiply the height component by 0.025 to convert  it from feet to metres.

--- .class #id 

## Links

[BMI Calculator](https://sanya14.shinyapps.io/BMICalc) - Shiny App

[BMI Documentation](https://sanya14.shinyapps.io/BMIDoc) - Shiny App Documentation

[server.R and ui.R](https://github.com/sanyabhogal24/BMICalc) - Link to Github repository


