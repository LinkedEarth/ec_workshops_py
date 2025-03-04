---
type: slides
---

<div><h1><img src="https://github.com/throughput-ec/ec-workshops/blob/main/static/module1/00_ec_slide1.png?raw=true" alt="EC Theme" width=25% align="left"/> Lesson 2<br>Project Organization</h1></div>

---

## Data analysis workflow 

![workflow](https://datacarpentry.org/rr-organization1/fig/workflow.png)

---

## Face it...

- There are going to be files

- LOTS of files

- The files will change over time

- The files will have relationships to each other

---

## For Your Inner Self

- File organization and naming is a mighty weapon against chaos

- Make a file's name and location VERY INFORMATIVE about what it is, why it exists, how it relates to other things

- The more things are self-explanatory, the better

---

## Organizing your data analysis workflow

**Raw data -> data**

Pick a strategy, any strategy, just pick one!

<div class="columns-2">

![workflow_raw_data_to_data](https://datacarpentry.org/rr-organization1/fig/workflow_raw_data_to_data.png)

~~~
data
data-raw
data-clean
data/
  - raw
  - clean
~~~

</div>

---

## Data -> results

Pick a strategy, any strategy, just pick one!

<div class="columns-2">

![workflow_data_to_results_1](https://datacarpentry.org/rr-organization1/fig/workflow_data_to_results_1.png)

~~~
code
scripts
analysis
bin
~~~
</div>

---

## Data -> results

Pick a strategy, any strategy, just pick one!

<div class="columns-2">

![workflow_data_to_results_2](https://datacarpentry.org/rr-organization1/fig/workflow_data_to_results_2.png)

~~~
figures
results
results/
  - figs
  - nums
figures
tables
~~~
</div>

---

## A real (and imperfect!) example

~~~
  /Users/jenny/research/bohlmann/White_Pine_Weevil_DE:
  total used in directory 246648 available 131544558
  drwxr-xr-x  14 jenny  staff        476 Jun 23  2014 .
  drwxr-xr-x   4 jenny  staff        136 Jun 23  2014 ..
  -rw-r--r--@  1 jenny  staff      15364 Apr 23 10:19 .DS_Store
  -rw-r--r--   1 jenny  staff  126231190 Jun 23  2014 .RData
  -rw-r--r--   1 jenny  staff      19148 Jun 23  2014 .Rhistory
  drwxr-xr-x   3 jenny  staff        102 May 16  2014 .Rproj.user
  drwxr-xr-x  17 jenny  staff        578 Apr 29 10:20 .git
  -rw-r--r--   1 jenny  staff         50 May 30  2014 .gitignore
  -rw-r--r--   1 jenny  staff       1003 Jun 23  2014 README.md
  -rw-r--r--   1 jenny  staff        205 Jun  3  2014 White_Pine_Weevil_DE.Rproj
  drwxr-xr-x  20 jenny  staff        680 Apr 14 15:44 analysis
  drwxr-xr-x   7 jenny  staff        238 Jun  3  2014 data
  drwxr-xr-x  22 jenny  staff        748 Jun 23  2014 model-exposition
  drwxr-xr-x   4 jenny  staff        136 Jun  3  2014 results
~~~

---

## Data

Ready to analyze data:

![sample_ready_to_analyze_data](https://datacarpentry.org/rr-organization1/fig/sample_ready_to_analyze_data.png)

<hr>

Raw data:

![sample_raw_data](https://datacarpentry.org/rr-organization1/fig/sample_raw_data.png)


---

## Analysis and figures

R scripts + the Markdown files from "Compile Notebook":

![sample_ready_to_analyze_data](https://datacarpentry.org/rr-organization1/fig/sample_ready_to_analyze_data.png)

<hr>

The figures created in those R scripts and linked in those Markdown files:

![sample_raw_data](https://datacarpentry.org/rr-organization1/fig/sample_raw_data.png)

## Scripts

Linear progression of R scripts, and Makefile to run the entire analysis:

![sample_scripts](https://datacarpentry.org/rr-organization1/fig/sample_scripts.png)

## Results

Tab-delimited files with one row per gene of parameter estimates, test statistics, etc.:

![sample_results](https://datacarpentry.org/rr-organization1/fig/sample_results.png)

## Expository files

Files to help collaborators understand the model we fit: some markdown docs, a Keynote presentation, Keynote slides exported as PNGs for viewability on GitHub:

![sample_expository](https://datacarpentry.org/rr-organization1/fig/sample_expository.png)

---

## Caveats / problems with this example

- This project is no where near done, i.e. no manuscript or publication-ready figs

- File naming has inconsistencies due to three different people being involved

- Code and reports/figures all sit together because it’s just much easier that way w/ knitr & rmarkdown

---

## Wins of this example

- I can walk away from the project and come back to it a year later and resume work fairly quickly

- The two other people were able to figure out what I did and decide which files they needed to look at, etc.

---

## Tip: Life cycle of data

Here’s how most data analyses go down in reality:

- You get raw data

- You explore, describe and visualize it

- You diagnose what this data needs to become useful

- You fix, clean, marshal the data into ready-to-analyze form

- You visualize it some more

- You fit a model or whatever and write lots of numerical results to file

- You make prettier tables and many figures based on the data & results accumulated by this point

Both the data file(s) and the code/scripts that acts on them reflect this progression

---

## Prepare data -> Do stats -> Make tables & figs

The R scripts:

~~~
01_marshal-data.r
02_pre-dea-filtering.r
03_dea-with-limma-voom.r
~~~

<hr>

The figures left behind:

~~~
02_pre-dea-filtering-preDE-filtering.png
03-dea-with-limma-voom-voom-plot.png
04_explore-dea-results-focus-term-adjusted-p-values1.png
04_explore-dea-results-focus-term-adjusted-p-values2.png
~~~

File organization should reflect inputs vs outputs and the flow of information

Source [Data Carpentry](https://datacarpentry.org/rr-organization1/02-file-organization/index.html)
---

# Let's Practice!