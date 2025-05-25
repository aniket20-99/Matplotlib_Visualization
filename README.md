# 📊 Matplotlib Visualization Gallery

An interactive collection of essential Matplotlib plots including Line Plot, Bar Chart, Scatter Plot, Histogram, Pie Chart, and Box Plot. This project uses a simple radio menu to let users explore visualizations dynamically.

# Matplotlib 

This project is all about Matplotlib, the basic data visualization tool of Python programming language. I have discussed Matplotlib object hierarchy, various plot types with Matplotlib and customization techniques associated with Matplotlib. 


This project is divided into various sections based on contents which are listed below:- 

## Table of Contents


1.	Introduction

2.	Overview of Python Data Visualization Tools

3.	Introduction to Matplotlib

4.	Import Matplotlib

5.	Displaying Plots in Matplotlib

6.	Matplotlib Object Hierarchy

7.	Matplotlib interfaces

8.	Pyplot API

9.	Object-Oriented API

10.	Figure and Subplots

11.	First plot with Matplotlib

12.	Multiline Plots

13.	Parts of a Plot

14.	Saving the Plot

15.	Line Plot

16.	Scatter Plot

17.	Histogram

18.	Bar Chart

19.	Horizontal Bar Chart

20.	Error Bar Chart

21.	Stacked Bar Chart

22.	Pie Chart

23.	Box Plot

24.	Area Chart

25.	Contour Plot

26.	Styles with Matplotlib Plots

27.	Adding a grid

28.	Handling axes

29.	Handling X and Y ticks

30.	Adding labels

31.	Adding a title

32.	Adding a legend

33.	Control colours

34.	Control line styles
 
35.	Summary

## 1. Introduction
When we want to convey some information to others, there are several ways to do so. The process of conveying the information with the help of plots and graphics is called **Data Visualization**. The plots and graphics take numerical data as input and display output in the form of charts, figures and tables. It helps to analyze and visualize the data clearly and make concrete decisions. It makes complex data more accessible and understandable. The goal of data visualization is to communicate information in a clear and efficient manner.
In this project, I shed some light on **Matplotlib**, which is the basic data visualization tool of Python programming language. Python has different data visualization tools available which are suitable for different purposes. First of all, I will list these data visualization tools and then I will discuss Matplotlib.

## 2. Overview of Python Visualization Tools
Python is the preferred language of choice for data scientists. Python have multiple options for data visualization. It has several tools which can help us to visualize the data more effectively. These Python data visualization tools are as follows:-
•	Matplotlib
•	Seaborn
•	pandas
•	Bokeh
•	Plotly - R PROGRAMING PACKAGE
•	ggplot - R PROGRAMING PACKAGE 
•	pygal - R programing pacakge 
In the following sections, I discuss Matplotlib as the data visualization tool. 

## 3. Introduction to Matplotlib
**Matplotlib** is the basic plotting library of Python programming language. It is the most prominent tool among Python visualization packages. Matplotlib is highly efficient in performing wide range of tasks. It can produce publication quality figures in a variety of formats.  It can export visualizations to all of the common formats like PDF, SVG, JPG, PNG, BMP and GIF. It can create popular visualization types – line plot, scatter plot, histogram, bar chart, error charts, pie chart, box plot, and many more types of plot. Matplotlib also supports 3D plotting. Many Python libraries are built on top of Matplotlib. For example, pandas and Seaborn are built on Matplotlib. They allow to access Matplotlib’s methods with less code. 

The project **Matplotlib** was started by John Hunter in 2002. Matplotlib was originally started to visualize Electrocorticography (ECoG) data of epilepsy patients during post-doctoral research in Neurobiology. The open-source tool Matplotlib emerged as the most widely used plotting library for the Python programming language. It was used for data visualization during landing of the Phoenix spacecraft in 2008.


## 4. Import Matplotlib
Before, we need to actually start using Matplotlib, we need to import it. We can import Matplotlib as follows:-
`import matplotlib`
Most of the time, we have to work with **pyplot** interface of Matplotlib. So, I will import **pyplot** interface of Matplotlib as follows:-
`import matplotlib.pyplot`
To make things even simpler, we will use standard shorthand for Matplotlib imports as follows:-
`import matplotlib.pyplot as plt`

## 5. Displaying Plots in Matplotlib
Viewing the Matplotlib plot is context based. The best usage of Matplotlib differs depending on how we are using it. 
There are three applicable contexts for viewing the plots. The three applicable contexts are using plotting from a script, plotting from an IPython shell or plotting from a Jupyter notebook.

### Plotting from a script
If we are using Matplotlib from within a script, then the **plt.show()** command is of great use. It starts an event loop, 
looks for all currently active figure objects, and opens one or more interactive windows that display the figure or figures.
The **plt.show()** command should be used only once per Python session. It should be used only at the end of the script. Multiple **plt.show()** commands can lead to unpredictable results and should mostly be avoided.

### Plotting from an IPython shell
We can use Matplotlib interactively within an IPython shell. IPython works well with Matplotlib if we specify Matplotlib mode. To enable this mode, we can use the **%matplotlib** magic command after starting ipython. Any plt plot command will cause a figure window to open and further commands can be run to update the plot.

### Plotting from a Jupyter notebook
- The Jupyter Notebook (formerly known as the IPython Notebook) is a data analysis and visualization tool that provides multiple tools under one roof.  It provides code execution, graphical plots, rich text and media display, mathematics formula and much more facilities into a single executable document.
- Interactive plotting within a Jupyter Notebook can be done with the **%matplotlib** command. There are two possible options to work with graphics in Jupyter Notebook. These are as follows:-

•	**%matplotlib notebook** – This command will produce interactive plots embedded within the notebook.

•	**%matplotlib inline** – It will output static images of the plot embedded in the notebook.
* After this command (it needs to be done only once per kernel per session), any cell within the notebook that creates a plot will embed a PNG image of the graphic.

## 6. Matplotlib Object Hierarchy
There is an Object Hierarchy within Matplotlib. In Matplotlib, a plot is a hierarchy of nested Python objects. 
A**hierarch** means that there is a tree-like structure of Matplotlib objects underlying each plot.

A **Figure** object is the outermost container for a Matplotlib plot. The **Figure** object contain multiple **Axes** objects. So, the **Figure** is the final graphic that may contain one or more **Axes**. The **Axes** represent an individual plot.

So, we can think of the **Figure** object as a box-like container containing one or more **Axes**. The **Axes** object contain smaller objects such as tick marks, lines, legends, title and text-boxes.

## 7.	Matplotlib API Overview

- Matplotlib has two APIs to work with. A MATLAB-style state-based interface and a more powerful object-oriented (OO) interface. 
- The former MATLAB-style state-based interface is called **pyplot interface** and the latter is called **Object-Oriented** interface.

- There is a third interface also called **pylab** interface. It merges pyplot (for plotting) and NumPy (for mathematical functions) together in an environment closer to MATLAB. This is considered bad practice nowadays. So, the use of **pylab** is strongly discouraged and hence, I will not discuss it any further.

## 8. Pyplot API 
**Matplotlib.pyplot** provides a MATLAB-style, procedural, state-machine interface to the underlying object-oriented library in Matplotlib. **Pyplot** is a collection of command style functions that make Matplotlib work like MATLAB. Each pyplot function makes some change to a figure - e.g., creates a figure, creates a plotting area in a figure etc. 

**Matplotlib.pyplot** is stateful because the underlying engine keeps track of the current figure and plotting area information and plotting functions change that information. To make it clearer, we did not use any object references during our plotting we just issued a pyplot command, and the changes appeared in the figure.


- We can get a reference to the current figure and axes using the following commands-

`plt.gcf ( )`   # get current figure

`plt.gca ( )`   # get current axes 

 
- **Matplotlib.pyplot** is a collection of commands and functions that make Matplotlib behave like MATLAB (for plotting). 
 - The MATLAB-style tools are contained in the pyplot (plt) interface. 

- This is really helpful for interactive plotting, because we can issue a command and see the result immediately. But, it is not suitable for more complicated cases. For these cases, we have another interface called **Object-Oriented** interface, described later.

## 9.	Object-Oriented API

- The **Object-Oriented API** is available for more complex plotting situations. It allows us to exercise more control over the figure. In Pyplot API, we depend on some notion of an "active" figure or axes. But, in the **Object-Oriented API** the plotting functions are methods of explicit Figure and Axes objects.
- **Figure** is the top level container for all the plot elements. We can think of the **Figure** object as a box-like container containing one or more **Axes**. 
- The **Axes** represent an individual plot. The **Axes** object contain smaller objects such as axis, tick marks, lines, legends, title and text-boxes.

### Objects and Reference

- The main idea with the **Object Oriented API** is to have objects that one can apply functions and actions on. The real advantage of this approach becomes apparent when more than one figure is created or when a figure contains more than one 
subplot.

- We create a reference to the figure instance in the **fig** variable. Then, we ceate a new axis instance **axes** using the 
**add_axes** method in the Figure class instance fig as follows:-

### Figure and Axes

- I start by creating a figure and an axes. A figure and axes can be created as follows:
`fig = plt.figure()`
`ax = plt.axes()`

- In Matplotlib, the **figure** (an instance of the class plt.Figure) is a single container that contains all the objects representing axes, graphics, text and labels. The **axes** (an instance of the class plt.Axes) is a bounding box with 
ticks and labels. It will contain the plot elements that make up the visualization. I have used the variable name fig 
to refer to a figure instance, and ax to refer to an axes instance or group of axes instances.

## 10. Figure and Subplots
- Plots in Matplotlib reside within a Figure object. As described earlier, we can create a new figure with plt.figure() 
as follows:-
- `fig = plt.figure()`
- Now, I create one or more subplots using fig.add_subplot() as follows:-
- `ax1 = fig.add_subplot(2, 2, 1)`
- The above command means that there are four plots in total (2 * 2 = 4). I select the first of four subplots (numbered from 1).
- I create the next three subplots using the fig.add_subplot() commands as follows:-

- `ax2 = fig.add_subplot(2, 2, 2)`
- `ax3 = fig.add_subplot(2, 2, 3)`
- `ax4 = fig.add_subplot(2, 2, 4)`

## 11. First plot with Matplotlib
- Now, I will start producing plots. Here is the first example:-
- `plt.plot([1, 3, 2, 4], 'b-')`
- This code line is the actual plotting command. Only a list of values has been plotted that represent the vertical coordinates of the points to be plotted. Matplotlib will use an implicit horizontal values list, from 0 (the first value) to N-1 (where N is the number of items in the list).

### Specify both Lists
- Also, we can explicitly specify both the lists as follows:- 
- `x3 = range(6)`
- `plt.plot(x3, [xi**2 for xi in x3])` 
- `plt.show()`

## 12.	Multiline Plots

- Multiline Plots mean plotting more than one plot on the same figure. We can plot more than one plot on the same figure.  
It can be achieved by plotting all the lines before calling show().

## 14.	Saving the Plot
- We can save the figures in a wide variety of formats. We can save them using the **savefig()** command as follows:-
- `fig.savefig(‘fig1.png’)`
- We can explore the contents of the file using the IPython **Image** object.
- `from IPython.display import Image`
- `Image(‘fig1.png’)`

- In **savefig()** command, the file format is inferred from the extension of the given filename. Depending on the backend, 
many different file formats are available. The list of supported file types can be found by using the get_supported_filetypes() method of the figure canvas object

## 15.	Line Plot
- We can use the following commands to draw the simple sinusoid line plot:-
 ### Create figure and axes first
- fig = plt.figure()
- ax = plt.axes()
### Declare a variable x5
- x5 = np.linspace(0, 10, 1000)
### Plot the sinusoid function
- ax.plot(x5, np.sin(x5), 'b-');

## 16.	Scatter Plot
- Another commonly used plot type is the scatter plot. Here the points are represented individually with a dot or a circle.


### Scatter Plot with plt.plot()
We have used plt.plot/ax.plot to produce line plots. We can use the same functions to produce the scatter plots

## 17.	Histogram
- Histogram charts are a graphical display of frequencies. They are represented as bars. They show what portion of the 
dataset falls into each category, usually specified as non-overlapping intervals. These categories are called bins.

- The **plt.hist()** function can be used to plot a simple histogram 

## 18.	Bar Chart
- Bar charts display rectangular bars either in vertical or horizontal form. Their length is proportional to the values they represent. They are used to compare two or more values.
- We can plot a bar chart using plt.bar() function.

## 19.	Horizontal Bar Chart
- We can produce Horizontal Bar Chart using the plt.barh() function. It is the strict equivalent of plt.bar() function.

## 20.	Error Bar Chart
- In experimental design, the measurements lack perfect precision. So, we have to repeat the measurements. It results in 
obtaining a set of values. The representation of the distribution of data values is done by plotting a single data point 
(known as mean value of dataset) and an error bar to represent the overall distribution of data.

- We can use Matplotlib's **errorbar()** function to represent the distribution of data values.

## 21. Stacked Bar Chart
- We can draw stacked bar chart by using a special parameter called **bottom** from the plt.bar() function.
- The optional **bottom** parameter of the plt.bar() function allows us to specify a starting position for a bar. Instead of running from zero to a value, it will go from the bottom to value. The first call to plt.bar() plots the blue bars. The second call to plt.bar() plots the red bars, with the bottom of the red bars being at the top of the blue bars.


## 22. Pie Chart

- Pie charts are circular representations, divided into sectors. The sectors are also called **wedges**. The arc length of each sector is proportional to the quantity we are describing. It is an effective way to represent information when we are interested mainly in comparing the wedge against the whole pie, instead of wedges against each other.

- Matplotlib provides the **pie()** function to plot pie charts from an array X. Wedges are created proportionally, so that each value x of array X generates a wedge proportional to x/sum(X).

## 23. Boxplot
- Boxplot allows us to compare distributions of values by showing the median, quartiles, maximum and minimum of a set of values.
- We can plot a boxplot with the **boxplot()** function

## 24. Area Chart
- An **Area Chart** is very similar to a **Line Chart**. The area between the x-axis and the line is filled in with color or shading. It represents the evolution of a numerical variable following another numerical variable.

## 25. Contour Plot
- **Contour plots** are useful to display three-dimensional data in two dimensions using contours or color-coded regions.
- **Contour lines** are also known as **level lines** or **isolines**. **Contour lines** for a function of two variables are 
curves where the function has constant values. They have specific names beginning with iso- according to the nature of the variables being mapped.


- There are lot of applications of **Contour lines** in several fields such as meteorology(for temperature, pressure, rain, wind
speed), geography, magnetism, engineering, social sciences and so on.

- The density of the lines indicates the **slope** of the function. The **gradient** of the function is always perpendicular to the contour lines. When the lines are close together, the length of the gradient is large and the variation is steep.
- A **Contour plot** can be created with the **plt.contour()** function
- The **contour()** function draws contour lines. It takes a 2D array as input.Here, it is a matrix of 10 x 20 random elements.
- The number of level lines to draw is chosen automatically, but we can also specify it as an additional parameter, N.
- `plt.contour(matrix, N)`

## 26. Styles with Matplotlib Plots

- The Matplotlib version 1.4 which was released in August 2014 added a very convenient `style` module. It includes a number of 
new default stylesheets, as well as the ability to create and package own styles.
- We can view the list of all available styles by the following command.
- `print(plt.style.availabe)`

## 27. Adding a grid
- In some cases, the background of a plot was completely blank. We can get more information, if there is a reference system in the plot. The reference system would improve the comprehension of the plot. An example of the reference system is adding a **grid**.
- We can add a grid to the plot by calling the **grid()** function. It takes one parameter, a Boolean value, to enable(if True)
or disable(if False) the grid.

## 28. Handling axes
- Matplotlib automatically sets the limits of the plot to precisely contain the plotted datasets. Sometimes, we want to set the
axes limits ourself. We can set the axes limits with the **axis()** function

### We can see that we now have more space around the lines.
- If we execute **axis()** without parameters, it returns the actual axis limits.
- We can set parameters to **axis()** by a list of four values. 
- The list of four values are the keyword arguments [xmin, xmax, ymin, ymax] allows the minimum and maximum limits for X and Y 
axis respectively.
- We can control the limits for each axis separately using the `xlim()` and `ylim()` functions.

## 29. Handling X and Y ticks

- Vertical and horizontal ticks are those little segments on the axes, coupled with axes labels, used to give a reference system
on the graph.So, they form the origin and the grid lines.
- Matplotlib provides two basic functions to manage them - **xticks()** and **yticks()**.
- Executing with no arguments, the tick function returns the current ticks' locations and the labels corresponding to each of them.
- We can pass arguments(in the form of lists) to the ticks functions. The arguments are:-

1. Locations of the ticks
2. Labels to draw at these locations.

## 30. Adding labels
- Another important piece of information to add to a plot is the axes labels, since they specify the type of data we are plotting.

## 31. Adding a title
- The title of a plot describes about the plot. Matplotlib provides a simple function **title()** to add a title to an image.

## 32. Adding a legend
- Legends are used to describe what each line or curve means in the plot. 
- Legends for curves in a figure can be added in two ways. One method is to use the **legend** method of the axis object and 
pass a list/tuple of legend texts
- A better method is to use the **label** keyword argument when plots are added to the figure. Then we use the **legend** method without arguments to add the legend to the figure. 
- The advantage of this method is that if curves are added or removed from the figure, the legend is automatically updated accordingly.

-  The **legend** function takes an optional keyword argument **loc**. It specifies the location of the legend to be drawn. 
-  The **loc** takes numerical codes for the various places the legend can be drawn. The most common **loc** values are as follows:-

-  ax.legend(loc=0)  # let Matplotlib decide the optimal location
- ax.legend(loc=1)  # upper right corner
- ax.legend(loc=2)  # upper left corner
- ax.legend(loc=3)  # lower left corner
- ax.legend(loc=4)  # lower right corner
- ax.legend(loc=5)  # right
- ax.legend(loc=6)  # center left
- ax.legend(loc=7)  # center right
- ax.legend(loc=8)  # lower center
- ax.legend(loc=9)  # upper center
- ax.legend(loc=10) # center

## 33. Control colours
- We can draw different lines or curves in a plot with different colours. In the code below, we specify colour as the last argument to draw red, blue and green lines.

### The colour names and colour abbreviations are given in the following table:-


**Colour Abbreviation** | **Colour Name**
:----------------------:|:----------------:
b                      | blue  
c                      | cyan  
g                      | green  
k                      | black  
m                      | magenta  
r                      | red  
w                      | white  
y                      | yellow  


###There are several ways to specify colours, other than by colour abbreviations:
    
•	The full colour name, such as yellow

•	Hexadecimal string such as ##FF00FF

•	RGB tuples, for example (1, 0, 1)

•	Grayscale intensity, in string format such as ‘0.7’.

## 34. Control line styles
- Matplotlib provides us different line style options to draw curves or plots. In the code below, I use different line styles 
to draw different plots.

- All the available line styles are available in the following table:

**Style Abbreviation** | **Style**
:---------------------:|:----------------:
-                     | solid line  
--                    | dashed line  
-.                    | dash-dot line  
:                     | dotted line  

- Now, we can see the default format string for a single line plot is 'b-'.

## 35. Summary

- In this project, I discuss Matplotlib (the basic plotting library in Python) and throw some light on various charts and customization techniques associated with it
- In particular, I discuss Matplotlib object hierarchy, Matplotlib architecture, Pyplot and Object-Oriented architecture. I also discuss subplots which is very important tool to create graphics in Matplotlib.
- Then, I discuss various types of plots like line plot, scatter plot, histogram, bar chart, pie chart, box plot, area chart and contour plot. 
- Finally, I discuss various customization techniques. I discuss how to customize the graphics with styles. I discuss how to add a grid and how to handle axes and ticks. I discuss how to add labels, title and legend. I discuss how to customize the charts with colours and line styles.
