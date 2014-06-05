R you ready to ggplot2?
========================================================
author: Understanding the Grammar of Graphics
transition: rotate
transition-speed: slow
width: 1440
height: 900
incremental: true
date: June 05, 2014
css: ./theme/my_style.css

<small> Tony Fujs </small>





========================================================
type: practice
incremental: false

# Objective:
# Get familiar with the logic of the Grammar of Graphics framework.

========================================================
type: practice
incremental: false

# Let's start with something everyone is familiar with...


========================================================
incremental: false
type: practice

## PRACTICE TIME!!

![](./tof/height.png)

## Draw a scatter plot of this dataset

========================================================
incremental: false
type: practice

## PRACTICE TIME!!

![](./tof/height.png)

## Think about the steps you took to draw your plot

========================================================
type: practice
incremental: false

# You probably did something along these lines...

Scatter plots: STEP 1
========================================================
left: 75%

![](./tof/gg1.png)

***

<q>First, you looked at your __data__.</q>

Scatter plots: STEP 2
========================================================
left: 75%

![](./tof/gg2.png)

***

<q>Then, you probably drew the axes of your plot. In the grammer of graphics framework. This is called a __coordinate system__ </q>

Scatter plots: STEP 3
========================================================
left: 75%

![](./tof/gg3.png)

***

<q>Next, you decided whether "height" should be represented on the x or y axis. In the world of the grammar of graphics, this is known as mapping variables to __aesthetics__. Aesthetics can be positions (x and y axis), but also things like size, color, shape, etc.</q>

Scatter plots: STEP 4
========================================================
left: 75%

![](./tof/gg4.png)

***

<q>After that, you had to define a __scale__ to map your variables on your sheet of paper, and adequately draw tickmarks on your x and y axes. 

Scatter plots: STEP 5
========================================================
left: 75%

![](./tof/gg5.png)

***

<q>Finally, you represented each row in the table, by a point on your plot. In the grammar of graphics world, data are represented with __geometric objects__. Geometric objects can be point, bar, line, etc.


Congratulations!!
========================================================
left: 65%

![](./tof/ggtab1.png)

***

<q>You just __identified 5 of 7 key elements of the grammar of graphics__. Almost any -2d- plot can be represented by specifying adequately each one of these 7 elements.</q>

========================================================
type: practice
incremental: false

# Let's take a closer look at each element separately

Slide structure
====================================
type: practice
incremental: false

* Data set goes here:

```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```


* Code goes here:
<pre><code class="r">simplified R code</code></pre>

***

* Plot goes here:
<img src="index-figure/unnamed-chunk-2.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



DATA
====================================

![](./tof/ggtab_data.png)

DATA
====================================



```
  year state stores
1 2005    FL    174
2 2005    MI     76
3 2005    NJ     41
4 2005    NV     22
5 2005    VT      4
```


<pre><code class="r"><b>data = mini_walmart</b></code></pre>

***

<q>Specifying your data set is really straightforward. If you want to visualize a data set named, say, "mini\_walmart", you only need to write: __data = mini_walmart__</q>

AESTHETIC MAPPING
====================================

![](./tof/ggtab_aes.png)


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


<pre><code class="r">
<b>aes(x = state,y = stores)</b>
data = mini_walmart
</code></pre>

***

<q>Mapping variables to aesthetics is also fairly straightforward. If you want to have "state" on the x axis, you simply specify:  __x = state__</q>

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


<pre><code class="r">
<b>aes(x = state,y = stores)</b>
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-6.png" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = state,y = stores,
   <b>color = stores</b>)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-8.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = state,y = stores,
   <b>color = states</b>)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-10.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = state,y = stores,
  <b>shape = state</b>)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-12.png" title="plot of chunk unnamed-chunk-12" alt="plot of chunk unnamed-chunk-12" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
<b>#COMPLETE THE CODE TO PRODUCE THIS PLOT</b>
aes(x = state,y = stores)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-14.png" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
#COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores,
   <b>color = state,
   shape = state</b>)
data = mini_walmart
</code></pre>

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


<pre><code class="r">
<b># WHAT ADDITIONAL AESTHETIC MAPPING IS NEEDED TO PRODUCE THIS PLOT?</b>
aes(x = state,y = stores)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-18.png" title="plot of chunk unnamed-chunk-18" alt="plot of chunk unnamed-chunk-18" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
# WHAT ADDITIONAL AESTHETIC MAPPING IS NEEDED TO PRODUCE THIS PLOT?
aes(x = state,y = stores,
   <b>size = stores</b>)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-20.png" title="plot of chunk unnamed-chunk-20" alt="plot of chunk unnamed-chunk-20" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-22.png" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart 
<b>scale_y_continuous()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-24.png" title="plot of chunk unnamed-chunk-24" alt="plot of chunk unnamed-chunk-24" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart 
<b>scale_y_log10()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-26.png" title="plot of chunk unnamed-chunk-26" alt="plot of chunk unnamed-chunk-26" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores,
   <b>color = stores</b>)
data = mini_walmart 
</code></pre>

***

<img src="index-figure/unnamed-chunk-28.png" title="plot of chunk unnamed-chunk-28" alt="plot of chunk unnamed-chunk-28" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores,
    color = stores)
data = mini_walmart
<b>scale_color_continuous()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-30.png" title="plot of chunk unnamed-chunk-30" alt="plot of chunk unnamed-chunk-30" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores,
    color = stores)
data = mini_walmart
<b>scale_color_continuous(
  low = 'light green',
  high = 'dark green')</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-32.png" title="plot of chunk unnamed-chunk-32" alt="plot of chunk unnamed-chunk-32" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


DON'T FORGET...
====================================
type: practice

1. ONE aesthetic = ONE scale
2. TWO aesthetics = TWO scales
3. THREE aesthetics = THREE scales...
4. ... you get the idea!


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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-34.png" title="plot of chunk unnamed-chunk-34" alt="plot of chunk unnamed-chunk-34" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_point()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-36.png" title="plot of chunk unnamed-chunk-36" alt="plot of chunk unnamed-chunk-36" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_bar()</b>
</code></pre>

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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_bar()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-39.png" title="plot of chunk unnamed-chunk-39" alt="plot of chunk unnamed-chunk-39" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
<b># COMPLETE THE CODE TO PRODUCE THIS PLOT</b>
aes(x = state,y = stores)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-41.png" title="plot of chunk unnamed-chunk-41" alt="plot of chunk unnamed-chunk-41" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
# COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores)
data = mini_walmart
<b>geom_line()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-43.png" title="plot of chunk unnamed-chunk-43" alt="plot of chunk unnamed-chunk-43" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_text()</b>
</code></pre>

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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_text()</b>
</code></pre>

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


<pre><code class="r">
aes(x = state,y = stores)
data = mini_walmart
<b>geom_text()</b>
</code></pre>

***

<q>What happened here? ggplot2 knows what a point is. It also knows what a bar is. However, when you tell ggplot2 to use __text__ to represent your data, ggplot2 doesn't know __which text__ to display... This needs to be explicitly specified.</q>


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


<pre><code class="r">
aes(x = state,y = stores,
  <b>label = stores</b>)
data = mini_walmart
geom_text()
</code></pre>

***

<img src="index-figure/unnamed-chunk-48.png" title="plot of chunk unnamed-chunk-48" alt="plot of chunk unnamed-chunk-48" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



Position adjustment: identity
====================================
left: 65%


![](./tof/ggtab_pos.png)

***

<q>Geometric objects sometimes overlap. The __position adjustment__ is another key element of the Grammar of Graphics that specifically addresses this issue</q>

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


<pre><code class="r">
aes(x = year,y = stores)
data = mini_walmart
geom_point()
</code></pre>

***

<img src="index-figure/unnamed-chunk-50.png" title="plot of chunk unnamed-chunk-50" alt="plot of chunk unnamed-chunk-50" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores)
data = mini_walmart
geom_point()
<b>position = 'identity'</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-52.png" title="plot of chunk unnamed-chunk-52" alt="plot of chunk unnamed-chunk-52" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores)
data = mini_walmart
<b>geom_bar()
position = identity</b>
</code></pre>

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


<pre><code class="r">
aes(x = year,y = stores)
data = mini_walmart
geom_bar()
<b>position = identity</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-55.png" title="plot of chunk unnamed-chunk-55" alt="plot of chunk unnamed-chunk-55" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


Position adjustment: identity
====================================
incremental: false
<q>Why do we have only 1 bar instead of 5? In reality, there are 5 bars on this plot, but since they __overlap__ and are of the __same color__, we cannot distinguish them.</q>

## Let's add some colors!

***

<img src="index-figure/unnamed-chunk-56.png" title="plot of chunk unnamed-chunk-56" alt="plot of chunk unnamed-chunk-56" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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


<pre><code class="r">
aes(x = year,y = stores,
   <b>fill = state</b>)
data = mini_walmart
geom_bar()
position = identity
</code></pre>

***

<img src="index-figure/unnamed-chunk-58.png" title="plot of chunk unnamed-chunk-58" alt="plot of chunk unnamed-chunk-58" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
   fill = state)
data = mini_walmart
geom_bar()
<b>position = dodge</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-60.png" title="plot of chunk unnamed-chunk-60" alt="plot of chunk unnamed-chunk-60" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
<b>position = stack</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-62.png" title="plot of chunk unnamed-chunk-62" alt="plot of chunk unnamed-chunk-62" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
<b>position = fill</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-64.png" title="plot of chunk unnamed-chunk-64" alt="plot of chunk unnamed-chunk-64" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
   fill = state)
data = mini_walmart
geom_bar()
position = fill
</code></pre>

***

<img src="index-figure/unnamed-chunk-66.png" title="plot of chunk unnamed-chunk-66" alt="plot of chunk unnamed-chunk-66" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
   fill = state)
data = mini_walmart
geom_bar()
position = fill
<b>coord_cartesian()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-68.png" title="plot of chunk unnamed-chunk-68" alt="plot of chunk unnamed-chunk-68" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
<b>coord_polar()</b>
</code></pre>

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


<pre><code class="r">
aes(x = year,y = stores,
    fill = state)
data = mini_walmart
geom_bar()
position = fill
<b>coord_polar()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-71.png" title="plot of chunk unnamed-chunk-71" alt="plot of chunk unnamed-chunk-71" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



COORDINATE SYSTEM: cartesian
====================================
incremental: false

<q>__pie chart = stacked bar chart__ in polar coordinates coordinate system!</q>

***

<img src="index-figure/unnamed-chunk-72.png" title="plot of chunk unnamed-chunk-72" alt="plot of chunk unnamed-chunk-72" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


====================================
incremental: false
type: practice

## PRACTICE TIME!!

![](./tof/height.png)

## Add a regression line to your hand drawn scatter plot

====================================
incremental: false
type: practice

## PRACTICE TIME!!

![](./tof/height.png)

## What additional step do you need to take?

STATISTICAL TRANSFORMATION
====================================
left: 65%

![](./tof/gg7.png)

***

<q>In order to plot your regression line, you first need to estimate this regression line, and compute the __predicted values__ for your dataset.</q> 

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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
geom_point()
</code></pre>

***

<img src="index-figure/unnamed-chunk-74.png" title="plot of chunk unnamed-chunk-74" alt="plot of chunk unnamed-chunk-74" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
geom_point(<b>stat = 'identity'</b>)
</code></pre>

***

<img src="index-figure/unnamed-chunk-76.png" title="plot of chunk unnamed-chunk-76" alt="plot of chunk unnamed-chunk-76" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
geom_point(<b>stat = 'smooth'</b>)
</code></pre>

***

<img src="index-figure/unnamed-chunk-78.png" title="plot of chunk unnamed-chunk-78" alt="plot of chunk unnamed-chunk-78" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
<b>geom_line</b>(stat = 'smooth')
</code></pre>

***

<img src="index-figure/unnamed-chunk-80.png" title="plot of chunk unnamed-chunk-80" alt="plot of chunk unnamed-chunk-80" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
<b>geom_point(stat = 'identity')</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-82.png" title="plot of chunk unnamed-chunk-82" alt="plot of chunk unnamed-chunk-82" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />



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


<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
<b>geom_point(stat = 'identity') +
geom_line(stat = 'smooth')</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-84.png" title="plot of chunk unnamed-chunk-84" alt="plot of chunk unnamed-chunk-84" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


LAYER
====================================

![](./tof/ggtab_layer.png)


LAYER
====================================
type: practice

## In the Grammar of Graphics framework, one plot is made of:
* ONE coordinate system
* As many scales as there are aesthetics
* ONE or MULTIPLE layers
