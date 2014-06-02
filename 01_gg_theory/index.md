Ggplot2: R you ready?
========================================================
author: Understanding the Grammar to Graphics (gg) framework
transition: rotate
transition-speed: slow
width: 1440
height: 900
incremental: true
date: June 02, 2014
css: ./theme/my_style.css


<small> Tony Fujs </small>





========================================================
<q>Ggplot2 is an __amazing__ tool for static data visualization. It is not necessarily obvious to realize how powerful it is until you get a strong understanding of its underlying logic though: The Grammar of Graphics. Using ggplot2 without understanding its underlying logic is possible, like going to see a 3D movie without your 3D glasses... You can certainly do it, but don't expect to get the full experience.</q>

How do we do it?
========================================================
incremental: false

1. gg theory

***

![](./tof/emmet.jpg)



========================================================
incremental: false
type: practice

PRACTICE TIME!!

![](./tof/height.png)

DRAW A SCATTER PLOT OF THE FOLLOWING DATASET

========================================================
incremental: false
type: practice

PRACTICE TIME!!

![](./tof/height.png)

DESCRIBE THE STEPS YOU TOOK TO DRAW THE PLOT

Scatter plots: STEP 1
========================================================

![](./tof/gg1.png)

Scatter plots: STEP 2
========================================================

![](./tof/gg2.png)

Scatter plots: STEP 3
========================================================

![](./tof/gg3.png)

Scatter plots: STEP 4
========================================================

![](./tof/gg4.png)

Scatter plots: STEP 5
========================================================

![](./tof/gg5.png)


Grammar of graphic summary
========================================================

![](./tof/ggtab1.png)

DATA
====================================


![](./tof/ggtab_data.png)

Data
====================================



```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```

* Code

```r
data = mini_walmart
```

***
AESTHETIC MAPPING
====================================


![](./tof/ggtab_aes.png)

Aesthetics: position
====================================



```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```


```r
aes(x = state,y = stores)
data = mini_walmart
```

***

Aesthetics: position
====================================
incremental: false



```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```


```r
aes(x = state,y = stores)
data = mini_walmart
```

***

<img src="index-figure/unnamed-chunk-7.png" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

Aesthetics: color
====================================



```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```


```r
aes(x = state,y = stores,
    color = stores)
data = mini_walmart
```

***


































































































































































































































































```
Error in scale$trans$breaks(limits) : could not find function "extended"
```
