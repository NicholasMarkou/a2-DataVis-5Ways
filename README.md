
![penguins](https://github.com/cs4804-24c/a2-DataVis-5Ways/assets/412089/accc5680-3c77-4d29-9502-d3ff8cd922af)


# Google Sheets

![Google Sheet](/googlesheets/google_sheets.png)
Google sheets provides a simple way to take a CSV of data and plot it on a graph with no programming experience. I found it very simple to create the graph. I first selected the range and pressed insert -> chart. I had to modify a few settings, as certain columns were used for wrong parts of the graph. Once selecting the correct column, the graph was almost complete. I then changed the styling of each series to match the colors in the README example, and ensured they had 80% opacity. I then added in labels and a legend. Unfortunately, it was not possible to have Google Sheets generate a size legend for the bubbles, which represent the bill length. Additionally, I was not able to scale the bubbles down. Currently, they are to large to make out the actual bill size of each bubble because of the large amount of overlapping. 

## Design Achievment using Google Sheets
I was able to use the color selector tool in Google Sheets to match the colors directly provided in the example screenshot provided by the Professor.

# Flourish

![Flourish](/Flourish/FlourishGraph.png)

For Flourish, I was easily able to create a similar graph to the example provided. This tool provided more flexibility than Google Sheets, and I did not need to look at any guides on how to use the tool. One notable difference was the ease of modifying the scaling of each individual scatter point. This prevented the overcrowding issue which occured within Google Sheets. I was unable to add a legend for the scale of each scatter point, similarly to Google Sheets. After using Flourish, I think it's good for simple graphs that look better than Google Sheets, but it's still limited with what parts of the graph can be modified. 

## Technical Achievment
I was able to add a popup box when a scatter point is clicked on.
![Popup](/Flourish/popupExample.png)

# matplotlib

![Matplotlob](/matplotlib/matplotlibfigure.png)

For the first coding based scatter plot, I utilized matplotlib, and used pandas to load the CSV into python. To prevent issue with matplotlib, I first dropped all rows that had NAN as a value. To get the correct colors per plot, I had to setup a dictionary that contained the species and the hex color from each. Then, I had to iterate through each species in the CSV, and plot each unique species with the color defined in the dictionary. It was very easy setting the labels, legend and grid as they only required one function call each. Once the setup was finished, calling the show function gave the popup of the chart. I think matplotlib can be useful to make quick graphs from collected data within a python script, as most of the difficulty came from reading in the file and manipulating it to be easily handled by matplotlib. Configuring the graph was simple. 

## Design Achievment

- Added gridlines
- Moved the default legend location to not coverup any datapoints

## Technical Achievment

- Output figure to a png file when script is ran

# Altair

![Altair](/altair/visualization.png)

# d3

Resources used:
- https://d3-graph-gallery.com/graph/scatter_basic.html
- Used my a1 submission as starter code



# 02-DataVis-5ways

Assignment 2 - Data Visualization, 5 Ways  
===

Now that you have successfully made a "visualization" of shapes and lines using d3, your next assignment is to successfully make a *actual visualization*... 5 times. 

The goal of this project is to gain experience with as many data visualization libraries, languages, and tools as possible.

I have provided a small dataset about penguins, `penglings.csv`.
Each row contains a penguin observation and several variables about it, including bill length, flipper length, and more.

Your goal is to use 5 different tools to make the following chart:

![](img/ggplot2.png)

These features should be preserved as much as possible in your replication:

- Data positioning: it should be a upward-trending scatterplot as shown.  Flipper Length should be on the x-axis and Body Mass on the y-axis.
- Scales: Note the scales do not start at 0.
- Axis ticks and labels: both axes are labeled and there are tick marks at a reasonable interval, e.g 10, 20, 30, etc.
- Color mapping to species.
- Size mapping to Bill Length.
- Opacity of circles set to 0.8 or similar for a semi-transparent effect.

Other features are not required. This includes:

- The background grid.
- The legends.

Note that some software packages will make it **impossible** to perfectly preserve the above requirements. 
Be sure to note where these deviate as you reflect on what a tool is good for.

Improvements are also welcome as part of Technical and Design achievements.

Libraries, Tools, Languages
---

You are required to use 5 different tools or libraries.
Of the 5 tools, you must use at least 3 libraries (libraries require code of some kind).
This could be `Python, R, Javascript`, or `Java, Javascript, Matlab` or any other combination.
Dedicated tools (i.e. Excel) do not count towards the language requirement.

Otherwise, you should seek tools and libraries to fill out your 5.

Below are a few ideas. Do not limit yourself to this list!
There are new tools coming out every year and we may not have an exhaustive list of the latest and greatest.

Some may be difficult choices, like Matlab or SPSS, which require large installations, licenses, and occasionally difficult UIs.

I have marked a few that are strongly suggested.

- R + ggplot2 `<- definitely worth trying`
- Excel
- d3 `<- since the rest of the class uses this, we're requiring it`
- Altair `<- hugely popular python library. highly recommended `
- three.js `<- well, it's a 3d library. not really recommended, but could be interesting and fun`
- p5js `<- good for playing around. not really a chart lib`
- Tableau
- PowerBI
- Vega-lite <- `<- very interesting formal visualization model; might be the future of the field`
- Flourish <- `<- popular in recent years`
- DataWrapper <- `<- popular in recent years`
- GNUplot `<- the former CS department head uses this all the time :)`
- SAS/SPSS/Matlab

You may write everything from scratch, or start with demo programs from books or the web. 
If you do start with code that you found, please identify the source of the code in your README and, most importantly, make non-trivial changes to the code to make it your own so you really learn what you're doing. 

Tips
---

- If you're using d3, key to this assignment is knowing how to load data.
You will likely use the [`d3.json` or `d3.csv` functions](https://d3js.org/d3-dsv) to load the data you found.

**Beware that these functions are *asynchronous*, meaning it's possible to "build" an empty visualization before the data actually loads. Figuring out how to do this properly can be a major hiccup if you haven't used async functions before. If this means you, start part of this project early so you don't end up in a rush!**

- *For web languages like d3* Don't forget to run a local webserver when you're debugging.
See my a1 video or online tutorials for how to do this.
Being able to host a local webserver is an essential web development skill and very common in visualization design as well.

Readme Requirements
---

A good readme with screenshots and structured documentation is required for this project. 
It should be possible to scroll through your readme to get an overview of all the tools and visualizations you produced.

- Each visualization should start with a top-level heading (e.g. `# d3`)
- Each visualization should include a screenshot. Put these in an `img` folder and link through the readme (markdown command: `![caption](img/<imgname>)`.
- Write a paragraph for each visualization tool you use. What was easy? Difficult? Where could you see the tool being useful in the future? Did you have to use any hacks or data manipulation to get the right chart?

Other Requirements
---

0. Your code should be forked from the GitHub repo.
1. Place all code, Excel sheets, etcetera in a named folder. For example, `r-ggplot, matlab, mathematica, excel` and so on.
2. Your writeup (readme.md in the repo) should also contain the following:

- Description of the Technical achievements you attempted with this visualization.
  - Some ideas include interaction, such as mousing over to see more detail about the point selected.
- Description of the Design achievements you attempted with this visualization.
  - Some ideas include consistent color choice, font choice, element size (e.g. the size of the circles).

GitHub Details
---

- Fork the GitHub Repository. You now have a copy associated with your username.
- Make changes to fulfill the project requirements. 
- To submit, make a [Pull Request](https://help.github.com/articles/using-pull-requests/) on the original repository.

Grading
---

Grades on a 120 point scale. 
24 points will be based on your Technical and Design achievements, as explained in your readme. 

Make sure you include the files necessary to reproduce your plots.
You should structure these in folders if helpful.
We will choose some at random to run and test.

**NOTE: THE BELOW IS A SAMPLE ENTRY TO GET YOU STARTED ON YOUR README. YOU MAY DELETE THE ABOVE.**

# R + ggplot2 + R Markdown

R is a language primarily focused on statistical computing.
ggplot2 is a popular library for charting in R.
R Markdown is a document format that compiles to HTML or PDF and allows you to include the output of R code directly in the document.

To visualized the cars dataset, I made use of ggplot2's `geom_point()` layer, with aesthetics functions for the color and size.

While it takes time to find the correct documentation, these functions made the effort creating this chart minimal.

![ggplot2](img/ggplot2.png)

# d3...

(And so on...)


## Technical Achievements
- **Proved P=NP**: Using a combination of...
- **Solved AI Forever**: ...

### Design Achievements
- **Re-vamped Apple's Design Philosophy**: As demonstrated in my colorscheme...
