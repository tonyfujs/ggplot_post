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

* Code
<pre><code class="r"><b>data = mini_walmart</b></code></pre>

***


AESTHETIC MAPPING
====================================

![](./tof/ggtab_aes.png)

AESTHETICS: POSITION
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
<b>aes(x = state,y = stores)</b>
data = mini_walmart
</code></pre>

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

<pre><code class="r">
<b>aes(x = state,y = stores)</b>
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-4.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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
   <b>color = states</b>)
data = mini_walmart
</code></pre>

***

<img src="index-figure/unnamed-chunk-8.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-10.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-12.png" title="plot of chunk unnamed-chunk-12" alt="plot of chunk unnamed-chunk-12" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-14.png" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-16.png" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-18.png" title="plot of chunk unnamed-chunk-18" alt="plot of chunk unnamed-chunk-18" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-20.png" title="plot of chunk unnamed-chunk-20" alt="plot of chunk unnamed-chunk-20" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<img src="index-figure/unnamed-chunk-22.png" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-24.png" title="plot of chunk unnamed-chunk-24" alt="plot of chunk unnamed-chunk-24" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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
    color = stores)
data = mini_walmart
<b>scale_color_continuous()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-28.png" title="plot of chunk unnamed-chunk-28" alt="plot of chunk unnamed-chunk-28" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-30.png" title="plot of chunk unnamed-chunk-30" alt="plot of chunk unnamed-chunk-30" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-32.png" title="plot of chunk unnamed-chunk-32" alt="plot of chunk unnamed-chunk-32" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-34.png" title="plot of chunk unnamed-chunk-34" alt="plot of chunk unnamed-chunk-34" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-37.png" title="plot of chunk unnamed-chunk-37" alt="plot of chunk unnamed-chunk-37" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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
# COMPLETE THE CODE TO PRODUCE THIS PLOT
aes(x = state,y = stores)
data = mini_walmart
<b>geom_line()</b>
</code></pre>

***

<img src="index-figure/unnamed-chunk-41.png" title="plot of chunk unnamed-chunk-41" alt="plot of chunk unnamed-chunk-41" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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
aes(x = state,y = stores,
  <b>label = stores</b>)
data = mini_walmart
geom_text()
</code></pre>

***

<img src="index-figure/unnamed-chunk-45.png" title="plot of chunk unnamed-chunk-45" alt="plot of chunk unnamed-chunk-45" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<pre><code class="r">
aes(x = year,y = stores)
data = mini_walmart
geom_point()
</code></pre>

***

<img src="index-figure/unnamed-chunk-47.png" title="plot of chunk unnamed-chunk-47" alt="plot of chunk unnamed-chunk-47" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-49.png" title="plot of chunk unnamed-chunk-49" alt="plot of chunk unnamed-chunk-49" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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
aes(x = year,y = stores,
   <b>fill = state</b>)
data = mini_walmart
geom_bar()
position = identity
</code></pre>

***

<img src="index-figure/unnamed-chunk-54.png" title="plot of chunk unnamed-chunk-54" alt="plot of chunk unnamed-chunk-54" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-60.png" title="plot of chunk unnamed-chunk-60" alt="plot of chunk unnamed-chunk-60" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-62.png" title="plot of chunk unnamed-chunk-62" alt="plot of chunk unnamed-chunk-62" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-64.png" title="plot of chunk unnamed-chunk-64" alt="plot of chunk unnamed-chunk-64" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-66.png" title="plot of chunk unnamed-chunk-66" alt="plot of chunk unnamed-chunk-66" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-68.png" title="plot of chunk unnamed-chunk-68" alt="plot of chunk unnamed-chunk-68" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-70.png" title="plot of chunk unnamed-chunk-70" alt="plot of chunk unnamed-chunk-70" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-72.png" title="plot of chunk unnamed-chunk-72" alt="plot of chunk unnamed-chunk-72" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-74.png" title="plot of chunk unnamed-chunk-74" alt="plot of chunk unnamed-chunk-74" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-77.png" title="plot of chunk unnamed-chunk-77" alt="plot of chunk unnamed-chunk-77" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

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

<pre><code class="r">
aes(x = stores, y = share)
data = mini_walmart
geom_point()
</code></pre>

***

<img src="index-figure/unnamed-chunk-79.png" title="plot of chunk unnamed-chunk-79" alt="plot of chunk unnamed-chunk-79" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-81.png" title="plot of chunk unnamed-chunk-81" alt="plot of chunk unnamed-chunk-81" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-83.png" title="plot of chunk unnamed-chunk-83" alt="plot of chunk unnamed-chunk-83" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-85.png" title="plot of chunk unnamed-chunk-85" alt="plot of chunk unnamed-chunk-85" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-87.png" title="plot of chunk unnamed-chunk-87" alt="plot of chunk unnamed-chunk-87" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />


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

<img src="index-figure/unnamed-chunk-89.png" title="plot of chunk unnamed-chunk-89" alt="plot of chunk unnamed-chunk-89" width="700" height="700" style="display: block; margin: auto 0 auto auto;" />

LAYER
====================================


![](./tof/ggtab_layer.png)
