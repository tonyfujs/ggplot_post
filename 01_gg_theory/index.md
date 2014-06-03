Dataviz with R
========================================================
author: ggplot2 & the grammar of graphics
transition: rotate
transition-speed: slow
width: 1440
height: 900
incremental: true
date: June 03, 2014
css: ./theme/my_style.css

<small> Tony Fujs </small>






========================================================
incremental: false

# Dataviz tools?

WHY USE R & ggplot2?
========================================================
* Flexible
* Powerful

WHY USE R & ggplot2?
========================================================
![](./tof/bike_ggplot.png)

WHY USE R & ggplot2?
========================================================
![](./tof/facebook.png)

WHY USE R & ggplot2?
========================================================
![](./tof/h_bullet_chart.png)

WHY USE R & ggplot2?
========================================================
* Flexible
* Powerful
* Scaling

Difference between this plot...
========================================================

![](./tof/simple_map.png)

and this plot?
========================================================

![](./tof/map.png)


ONE LINE OF CODE!!
========================================================

## facet_wrap(~year)

WHY USE R & ggplot2?
========================================================

* Flexible
* Powerful
* Scaling
* Reproducible work

WHY USE R & ggplot2?
========================================================
incremental: false

* Flexible
* Powerful
* Scaling
* Reproducible work
* Building block for other tools (lyra, ggvis, SPSS)


What is ggplot2?
========================================================
* R package (Tool in the R toolbox)
* Rely on the Grammar of Graphics (gg)

***

![](./tof/hadley.png)


Barriers to entry
========================================================
* R: From point & click to writing code
* Learning Grammar of Graphics (gg) - as opposed to typology


Objective of the workshop
========================================================

### Remove those barriers
* Understand the gg framework
* Play with simple code

How do we do it?
========================================================
incremental: false

1. gg theory

***

![](./tof/emmet.jpg)


How do we do it?
========================================================
incremental: false

1. gg theory
2. create simple plots

***

![](./tof/pos_id_bar.png)

How do we do it?
========================================================
incremental: false

1. gg theory
2. create simple plots
3. create complex plot(s)

***

![](./tof/map.png)


Napoleon's Russian Campaign: Original
========================================================

![](./tof/minard_map.png)

Napoleon's Russian Campaign: ggplot2
========================================================

![](./tof/minard_map_gg.png)


Small multiples: Walmart stores
========================================================

![](./tof/map.png)


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

<pre><code class="r">
ggplot() + 
geom_point(
 aes(x = state,y = stores),
 <b>data = mini_walmart</b>)
</code></pre>

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

<img src="index-figure/unnamed-chunk-10.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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
    color = state)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-13.png" title="plot of chunk unnamed-chunk-13" alt="plot of chunk unnamed-chunk-13" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


Aesthetics: shape
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
    shape = state)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-16.png" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


PRACTICE TIME!!
====================================
type: practice


```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```



```r
#COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-19.png" title="plot of chunk unnamed-chunk-19" alt="plot of chunk unnamed-chunk-19" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


PRACTICE TIME!!
====================================
type: practice
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
#COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores,
    color = state,
    shape = state)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-22.png" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


PRACTICE TIME!!
====================================
type: practice


```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```



```r
# WHAT ADDITIONAL AESTHETIC MAPPING IS NEEDED TO PRODUCE THIS PLOT?
aes(x = state,y = stores)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-25.png" title="plot of chunk unnamed-chunk-25" alt="plot of chunk unnamed-chunk-25" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


PRACTICE TIME!!
====================================
type: practice
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
# WHAT ADDITIONAL AESTHETIC MAPPING IS NEEDED TO PRODUCE THIS PLOT?
aes(x = state,y = stores,
    size = stores)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-28.png" title="plot of chunk unnamed-chunk-28" alt="plot of chunk unnamed-chunk-28" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


SCALE
====================================


![](./tof/ggtab_scale.png)

Scale: position (default)
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

<img src="index-figure/unnamed-chunk-31.png" title="plot of chunk unnamed-chunk-31" alt="plot of chunk unnamed-chunk-31" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


Scale: position (default)
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
scale_y_continuous()
```


***

<img src="index-figure/unnamed-chunk-34.png" title="plot of chunk unnamed-chunk-34" alt="plot of chunk unnamed-chunk-34" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Scale: position (log)
=====================================



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
scale_y_log10()
```


***

<img src="index-figure/unnamed-chunk-37.png" title="plot of chunk unnamed-chunk-37" alt="plot of chunk unnamed-chunk-37" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Scale: color
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
aes(x = state,y = stores,
    color = stores)
data = mini_walmart 
```


***

<img src="index-figure/unnamed-chunk-40.png" title="plot of chunk unnamed-chunk-40" alt="plot of chunk unnamed-chunk-40" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Scale: color
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
aes(x = state,y = stores,
    color = stores)
data = mini_walmart
scale_color_continuous()
```


***

<img src="index-figure/unnamed-chunk-43.png" title="plot of chunk unnamed-chunk-43" alt="plot of chunk unnamed-chunk-43" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Scale: color
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
scale_color_continuous(
  low = 'light green',
  high = 'dark green')
```


***

<img src="index-figure/unnamed-chunk-46.png" title="plot of chunk unnamed-chunk-46" alt="plot of chunk unnamed-chunk-46" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Geometric objects: point
===================================


![](./tof/ggtab_geom.png)


Geometric objects: point
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

<img src="index-figure/unnamed-chunk-49.png" title="plot of chunk unnamed-chunk-49" alt="plot of chunk unnamed-chunk-49" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Geometric objects: point
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
geom_point()
```


***

<img src="index-figure/unnamed-chunk-52.png" title="plot of chunk unnamed-chunk-52" alt="plot of chunk unnamed-chunk-52" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Geometric objects: bar
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
geom_bar()
```


***

TAKE A GUESS:
WHAT WILL THIS PLOT LOOK LIKE?


Geometric objects: bar
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
geom_bar()
```


***

<img src="index-figure/unnamed-chunk-57.png" title="plot of chunk unnamed-chunk-57" alt="plot of chunk unnamed-chunk-57" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



PRACTICE TIME!!
====================================
type: practice
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
# COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores)
data = mini_walmart
```


***

<img src="index-figure/unnamed-chunk-60.png" title="plot of chunk unnamed-chunk-60" alt="plot of chunk unnamed-chunk-60" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



PRACTICE TIME!!
====================================
type: practice
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
# COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores)
data = mini_walmart
geom_line()
```


***

<img src="index-figure/unnamed-chunk-63.png" title="plot of chunk unnamed-chunk-63" alt="plot of chunk unnamed-chunk-63" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Geometric objects: text
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
geom_text()
```


***

TAKE A GUESS:
WHAT WILL THIS PLOT LOOK LIKE?


Geometric objects: text
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
geom_text()
```


***

~~Error: geom_text requires the following missing aesthetics: label~~


Geometric objects: text
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
aes(x = state,y = stores,
    label = stores)
data = mini_walmart
geom_text()
```


***

<img src="index-figure/unnamed-chunk-70.png" title="plot of chunk unnamed-chunk-70" alt="plot of chunk unnamed-chunk-70" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
====================================


![](./tof/ggtab_pos.png)

Position adjustment: identity
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
aes(x = year,y = stores)
data = mini_walmart
geom_point()
```


***

<img src="index-figure/unnamed-chunk-73.png" title="plot of chunk unnamed-chunk-73" alt="plot of chunk unnamed-chunk-73" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores)
data = mini_walmart
geom_point()
position = 'identity'
```


***

<img src="index-figure/unnamed-chunk-76.png" title="plot of chunk unnamed-chunk-76" alt="plot of chunk unnamed-chunk-76" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores)
data = mini_walmart
geom_bar()
position = identity
```


***

TAKE A GUESS: WHAT WILL THIS PLOT LOOK LIKE?


Position adjustment: identity
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
aes(x = year,y = stores)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-81.png" title="plot of chunk unnamed-chunk-81" alt="plot of chunk unnamed-chunk-81" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-84.png" title="plot of chunk unnamed-chunk-84" alt="plot of chunk unnamed-chunk-84" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-87.png" title="plot of chunk unnamed-chunk-87" alt="plot of chunk unnamed-chunk-87" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-90.png" title="plot of chunk unnamed-chunk-90" alt="plot of chunk unnamed-chunk-90" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-93.png" title="plot of chunk unnamed-chunk-93" alt="plot of chunk unnamed-chunk-93" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-96.png" title="plot of chunk unnamed-chunk-96" alt="plot of chunk unnamed-chunk-96" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = identity
```


***

<img src="index-figure/unnamed-chunk-99.png" title="plot of chunk unnamed-chunk-99" alt="plot of chunk unnamed-chunk-99" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: dodge
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = dodge
```


***

<img src="index-figure/unnamed-chunk-102.png" title="plot of chunk unnamed-chunk-102" alt="plot of chunk unnamed-chunk-102" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: stack
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = stack
```


***

<img src="index-figure/unnamed-chunk-105.png" title="plot of chunk unnamed-chunk-105" alt="plot of chunk unnamed-chunk-105" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: fill
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
```


***

<img src="index-figure/unnamed-chunk-108.png" title="plot of chunk unnamed-chunk-108" alt="plot of chunk unnamed-chunk-108" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />






COORDINATE SYSTEM: cartesian
====================================


![](./tof/ggtab_coord.png)

COORDINATE SYSTEM: cartesian
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
```


***

<img src="index-figure/unnamed-chunk-111.png" title="plot of chunk unnamed-chunk-111" alt="plot of chunk unnamed-chunk-111" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



COORDINATE SYSTEM: cartesian
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
coord_cartesian()
```


***

<img src="index-figure/unnamed-chunk-114.png" title="plot of chunk unnamed-chunk-114" alt="plot of chunk unnamed-chunk-114" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



COORDINATE SYSTEM: cartesian
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
coord_polar()
```


***

TAKE A GUESS:
WHAT WILL THIS PLOT LOOK LIKE?


COORDINATE SYSTEM: cartesian
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
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
coord_polar()
```


***

<img src="index-figure/unnamed-chunk-119.png" title="plot of chunk unnamed-chunk-119" alt="plot of chunk unnamed-chunk-119" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


====================================
incremental: false
type: practice

PRACTICE TIME!!

![](./tof/height.png)

ADD A REGRESSION LINE TO YOUR HAND DRAWN SCATTER PLOT

STATISTICAL TRANSFORMATION
====================================


![](./tof/gg7.png)

STATISTICAL TRANSFORMATION
====================================


![](./tof/gg8.png)

STATISTICAL TRANSFORMATION
====================================


![](./tof/gg9.png)

STATISTICAL TRANSFORMATION
====================================


![](./tof/ggtab_stat.png)


STATISTICAL TRANSFORMATION: identity
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_point()
```


***

<img src="index-figure/unnamed-chunk-122.png" title="plot of chunk unnamed-chunk-122" alt="plot of chunk unnamed-chunk-122" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



STATISTICAL TRANSFORMATION: identity
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_point(stat = 'identity')
```


***

<img src="index-figure/unnamed-chunk-125.png" title="plot of chunk unnamed-chunk-125" alt="plot of chunk unnamed-chunk-125" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



STATISTICAL TRANSFORMATION: smooth
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_point(stat = 'smooth')
```


***

<img src="index-figure/unnamed-chunk-128.png" title="plot of chunk unnamed-chunk-128" alt="plot of chunk unnamed-chunk-128" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



STATISTICAL TRANSFORMATION: smooth
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_line(stat = 'smooth')
```


***

<img src="index-figure/unnamed-chunk-131.png" title="plot of chunk unnamed-chunk-131" alt="plot of chunk unnamed-chunk-131" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



LAYER
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_point(stat = 'identity')
```


***

<img src="index-figure/unnamed-chunk-134.png" title="plot of chunk unnamed-chunk-134" alt="plot of chunk unnamed-chunk-134" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



LAYER
====================================



```
  year state stores share
1 2005    FL    174  0.40
2 2005    MI     76  0.30
3 2005    NJ     41  0.15
4 2005    NV     22  0.10
5 2005    VT      4  0.05
```



```r
aes(x = stores, y = share)
data = mini_walmart
geom_point(stat = 'identity') +
geom_line(stat = 'smooth')
```


***

<img src="index-figure/unnamed-chunk-137.png" title="plot of chunk unnamed-chunk-137" alt="plot of chunk unnamed-chunk-137" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


LAYER
====================================


![](./tof/ggtab_layer.png)
