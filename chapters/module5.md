---
title: 'Module 5: Introduction to Matplotlib'
description:
  'This module will teach you how to use Matplotlib, a comprehensive library for creating static, animated, and
  interactive visualizations in Python. The module is structured around the visualization of two contemporaneous monthly timeseries: the NINO3 SST dataset and All India Rainfall.'
prev: /module4
next: /module6
type: chapter
id: 5
---

<exercise id="1" title="Introduction to Matplotlib">

Matplotlib is the go-to library for plotting within Python, with many functionalities and names reminiscent of Matlab's plotting libraries. Matplotlib comes with very good default parameters, so you can get visualizing within a few minutes of installing it. It is also extensively customizable, and can be used to make publication-quality graphics.

if you were to learn a single plotting tool to keep in your toolbox, this is the package.

The key feature to Matplotlib is its extensibility and the extensive [documentation](https://matplotlib.org) available to the community. Matplotlib underlies many other graphics libraries, including Cartopy (next chapter), and Pyleoclim, so it is essential that you understand a bit about it.


As before, we recommend looking over the [Pythia Matplotlib tutorial](https://foundations.projectpythia.org/core/matplotlib/matplotlib-basics.html) first. We recommend that you use the provided [Binder link](https://mybinder.org/v2/gh/ProjectPythia/pythia-foundations/main?urlpath=lab/tree/core/matplotlib/matplotlib-basics.ipynb) to follow along the article.

</exercise>

<exercise id="2" title="A first plot">

We start by loading and plotting the [NINO3 sea-surface temperature](https://climatedataguide.ucar.edu/climate-data/nino-sst-indices-nino-12-3-34-4-oni-and-tni) data. Notice that the code uses pandas (see Chapter 4) to load it; your job is to plot NINO3 vs time and annotate the plot by giving it appropriate labels (with units) and title.


<codeblock id="05_01">

Look up the documentation at https://matplotlib.org/stable/index.html!

</codeblock>

Notice that this call to the `subplots` method created:
-  a [figure](https://matplotlib.org/stable/api/figure_api.html?highlight=figure#module-matplotlib.figure) object `fig`
-  an [axes](https://matplotlib.org/stable/api/axes_api.html?highlight=axes#module-matplotlib.axes) object `ax`, to which the plot method is applied.  

For such a simple chart, the distinction is immaterial, but it will soon be important to distinguish between figure and axes, particularly when we create figures with multiple subplots.

If you wanted to change the size of the figure to 10 by 6 in, say, you would replace the first line of the figure by:
```
fig, ax = plt.subplots(figsize=(10, 6))
```
Give it a try!

</exercise>

exercise id="3" title="Plot customization">

We now explore Matplotlib's infinite customizability. All default parameters are stored in a dictionary called `rcParams`.
rc stands for "runtime configuration" and any changes to `plt.rcParams` will stay for all subsequent plots in your session. These parameters can be customised and [saved for later use](https://matplotlib.org/stable/tutorials/introductory/customizing.html#customizing-with-matplotlibrc-files).

For instance, the default figure size can be found as:
```
plt.rcParams['figure.figsize']
```
Typing this in your Binder should return `[6.0, 4.0]`


<codeblock id="05_02">

Look up the documentation at https://matplotlib.org/stable/index.html!

</codeblock>

</exercise>
