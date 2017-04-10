---
title       : Body Mass Index (BMI) Ckecker
subtitle    : Developing Data Products Project
author      : Daniel Crespo
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What is BMI?

The Body Mass Index (BMI) is a measure of body fat based on height and weight that applies to adult men and women.
Regarding the BMI measure, the **World Health Organization** (WHO) proposes the following classification:
* *BMI* < 18.5       : Underweight
* *BMI* [18.5 - 24.9] : Normal weight
* *BMI* [25 - 29.9]   : Overweight
* *BMI* >= 30        : Obesity

--- 

## How is it calculated?
There is a formula for calculating the *BMI* measure. The formula is the following:

*BMI* = Weight(kg) / Height(metres)$^2$

Thus for the next example, the *BMI* will be:


```r
bmi <- function(peso, altura) {
    return(peso / (altura ^ 2))
}

peso = 75
altura = 1.80

bmi(peso, altura)
```

```
## [1] 23.14815
```


---

## Diagnostic
The function use for calculating the diagnostic is the following: 
For our example (weight = 90 kg and height = 1.80 m) the diagnostic would be:

```r
resul <- function(peso, altura){
    bmi <- function(peso, altura) {
        return(peso / (altura ^ 2))
        }
    v.bmi <- bmi(peso, altura)
    
    if (v.bmi < 18.5) return("Underweight")
    else if (v.bmi < 24) return ("Normal weight")
    else if (v.bmi < 30) return ("Overweight")
    else return ("Obesity")
    
}

print(resul(90 , 1.8))
```

```
## [1] "Overweight"
```

---
## Conclusion
The BMI is a relatively easy, cheap and non-invasive method for establishing weight status, and for most people, it correlates reasonably well with their level of body fat. 

However, BMI is only a proxy for body fatness. other factors such as fitness, ethnic origin and puberty can alter the relation 
between BMI and body fatness and must be taken into consideration.

