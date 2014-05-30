---
title       : GG theory
subtitle    : Understanding the Grammar of Graphics framework
author      : Tony Fujs
job         : 
framework   : revealjs          # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js    # {highlight.js, prettify, highlight}
hitheme     : solarized_light # 
widgets     : []              # {mathjax, quiz, bootstrap}
mode        : selfcontained   # {standalone, draft}
width       : 1440
height      : 900
incremental : true
---



## Objective: Understand the gg framework

<q>Ggplot2 is an __amazing__ tool for static data visualization. It is not necessarily obvious to realize how powerful it is until you get a strong understanding of its underlying logic though: The Grammar of Graphics. Using ggplot2 without understanding its underlying logic is possible, like going to see a 3D movie without your 3D glasses... You can certainly do it, but don't expect to get the full experience.</q>

--- .centrepre &vcenter .bigger

## Setup

<a class='example'>Your Turn</a>
  
```
author("myDeck")
```

*** =pnotes

my notes about this slide


--- .class #id 

## PRACTICE TIME!!

![](./tof/height.png)

DRAW A SCATTER PLOT OF THE FOLLOWING DATASET

--- .class #id 


## PRACTICE TIME!!

![](./tof/height.png)

DESCRIBE THE STEPS YOU TOOK TO DRAW THE PLOT

--- .class #id

## Scatter plots: STEP 1

Start with your data set.

![](./tof/gg1.png)

--- .class #id

## Scatter plots: STEP 2

![](./tof/gg2.png)

--- .class #id

## Scatter plots: STEP 3

![](./tof/gg3.png)

--- .class #id

## Scatter plots: STEP 4

![](./tof/gg4.png)

--- .class #id

## Scatter plots: STEP 5

![](./tof/gg5.png)

--- .class #id

## Grammar of graphic summary

![](./tof/ggtab1.png)

--- .class #id

## DATA

![](./tof/ggtab_data.png)

--- .class #id

## Data


```
##   year state stores
## 1 2005    FL    174
## 2 2005    MI     76
## 3 2005    NJ     41
## 4 2005    NV     22
## 5 2005    VT      4
```

* Code

```r
data = mini_walmart
```

***

--- .class #id

## AESTHETIC MAPPING

![](./tof/ggtab_aes.png)

--- .class #id

## Aesthetics: position


```
##   year state stores
## 1 2005    FL    174
## 2 2005    MI     76
## 3 2005    NJ     41
## 4 2005    NV     22
## 5 2005    VT      4
```


```r
aes(x = state,y = stores)
data = mini_walmart
```

***

--- .class #id

## Next slide
