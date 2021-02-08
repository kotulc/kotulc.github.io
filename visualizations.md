---
layout: default
---

# *Visualizations* Project Page
The goal of this project is to create a convienent framework for combining and animating matplotlib components (subplots) concurrently. The final combined plot is akin to a dashboard with the single purpose of displaying multiple subplots, each with one or more different sources of sequential data.  

Component subplots may be updated on a step or sub-step schedule, meaning that select subplots can display information at different rates or resolutions. The sub-step animation support provides an additional layer of flexibilty when displaying sequential data that may have been collected at different intervals. For more information regarding use and functionality please see the project wiki page (this should be added shortly).  

Find the source for this project on [Github](https://github.com/kotulc/visualizations)  

<iframe width="560" height="315" src="https://www.youtube.com/embed/R8i-ZYlUobw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>    

## Getting Started
View the [latest documentation](https://visualizations.readthedocs.io/en/latest/) built with Sphinx hosted by [ReadTheDocs](https://readthedocs.org/).

Before using this framework, it is strongly suggested that you start by familiarizing yourself with Matplotlib's pyplot interface using the following [Matplotlib tutorial] (https://matplotlib.org/3.1.1/tutorials/introductory/pyplot.html).  

For ease of use, it is recommended that you setup a virtual environment to install and run this framework. 

If you haven't worked with virtual envionrmnets before, you may use a platform like [Anaconda or Miniconda](https://docs.anaconda.com/).


## Installation
Use the included requirements.txt to install all required dependencies:  
    
    pip install -r requirements.txt
    
Alternatively, if you want to run just the base subnet_plot module, you may be able to simply install Matplotlib:  
    
    pip install Matplotlib
    
Once you have installed the dependencies you can run some sample animations by calling subnet_plot. See the [project documentation](https://visualizations.readthedocs.io/en/latest/) for more details.  


## Subplot Components
A small selection of custom components are included to serve as an example of how to implement Matplotlib objects into this framework.  See below for a brief description of each class along with links to the relevant Matplotlib documentation.  

![line_bar_plot](/images/line_bar_plot.png)  

Above, a simple combined bar and line plot from `display_sample_plots()`.  


#### Bar subplot 
The bar subplot displays primary elements using the supplied colormap while displaying the optional secondary elements in grayscale.  

![bar_plot](/images/bar_plot.png)  

The SubplotBar class is based on the [Matplotlib bar](https://matplotlib.org/api/_as_gen/matplotlib.axes.Axes.bar.html) object.  


#### Line subplot 
The line subplot combines the basic line and bar plots. The optional bar data source is rendered behind the primary line data.  

![line_plot](/images/line_plot.png)  

The `SubplotLine` class is based on the [Matplotlib plot](https://matplotlib.org/api/_as_gen/matplotlib.axes.Axes.plot.html) object.  

#### Matrix subplot 
The matrix subplot renders a 2-dimensional array in sequential steps with optional 1-dimensional arrays affixed to the left and top sides of the central matrix.  

![matrix_plot](/images/matrix_plot.png)  

The `SubplotMatrix` class is based on the [Matplotlib image](https://matplotlib.org/api/image_api.html) object.  
Also see the [imshow axes](https://matplotlib.org/api/_as_gen/matplotlib.axes.Axes.imshow.html).  


#### Text subplot 
The text subplot displays data using a text-based readout. The primary data source is rendered within a table, while a secondary data source is displayed in rows below the primary table.  

![text_plot](/images/text_plot.png)  

The `SubplotText` class component is based on the [Matplotlib table](https://matplotlib.org/api/_as_gen/matplotlib.axes.Axes.table.html) object.  


#### Layouts and gridspec
The figure's grid-based layout is defined by the gridspec object passed to `add_subplot()` when adding subplot objects to the parent SubnetPlot.  

![combined_plot](/images/combined_plot.png)  

For a complete description of Matplotlib's gridspec please take a look at the [tutorial](https://matplotlib.org/3.1.1/tutorials/intermediate/gridspec.html).  


#### Styles and color maps
Each subplot component's style is defined by the tempalte `SubnetSubplot` class. Colormaps are used extensively to render plot elements. See the [colormap](https://matplotlib.org/3.1.1/gallery/color/colormap_reference.html) reference for valid values.  


### Screenshots
As of the current release, the following screenshots are from the subnet_visualize module:  

#### A network layer with an MNIST input sample  
![layer visualization](/images/layer_v8.1.png)  

#### A node specific combined representation  
![node visualization](/images/node_v8.3.png)  

#### The latest sample found in subnet_visualization  
![node visualization](/images/node_v8.4.png)  


### Below are a few samples of older visualizations from previous versions of this project:  
![layer visualization](/images/node_v2.3.png)  

#### An early node specific representation  
![layer visualization](/images/node_v4.0.png)  

#### A step-based display with node selection
![layer visualization](/images/node_v7.6.png)  
