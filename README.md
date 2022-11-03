# Personal assignment 
- due on 15th December 22 23.59h
- 25% of points for DIS08

In this assignment, you will prove your knowledge on open data, data formats, and working with data in python by implementing your first data analysis project.

Your task is, similar to what you did in the hands-on in L02, to choose a dataset from one of the three public open data sources [data.europa.eu](https://data.europa.eu/en), [govdata.de](https://www.govdata.de/), and [open.nrw](https://open.nrw/), and plan a data analysis project. This time though, you then will also perform the task yourself! 

This project includes the following sub-tasks:
1. **Selection of your dataset**
	- What dataset do you choose? (URL, name)
	- **Describe the dataset**: Variables, data format, collection period, who and why collected it, ...
	- What makes this dataset interesting to you?
2. **Conceptualisation of your application**. Define either
	- a task you want to perform,
	- a problem you want to solve, or 
	- a question which needs to be answered.
3.  Create a **private GitHub repository** and 
4.  Add us (kreutzch, HaakFab) **as collaborators** to the repository.
5. **Document** your train of thoughts in an outcome-oriented manner in a **structured markdown document** in your GitHub.
6. Select a **means of presenting your results**
	- **Discuss how your means of presentations helps to solve your task** 
	-  What **methods** do you have to employ? What **visualisations** help to illustrate your findings=
7. **Importing** your data in python
8. **Cleaning** your data
9. **Analysing** the data according to your chosen task and **visualise your results** to fulfil the needs of your concept from 2.
10.  on **15th December 22 at 23.59** your time for the project is up. **We will not take into consideration any edits after this deadline**, so make sure to push your final edits ahead of time! We will only regard files in the repository. You have to submit:
- For the concept: **At least one Markdown document**. You can also use the GitHub page structures and aspects discussed in the lectures.
- For your implementation: **A (jupyter) notebook**. **Use text blocks and/or comments**, to document your code! If you produce visualisations or other means of illustrating your findings, remember to save your notebook with the results.	 

Remember: You have to document everything in your markdown file(s), we cannot include anything that is not in there in our evaluation. We will not make assumptions in your favour. 

**DO NOT** use datasets from other sources and/or if there is already an application that you describe (this is why we did not include kaggle). To avoid problems, make sure to search for any other applications that are similar to your ideas and if there is something similar, either chose a different application or discuss the issue and why your application differs sufficiently from already existing applications.

## Evaluation criteria and Rating Matrix
We evaluate your projects based on two attributes:
1. **10 points: quality of your concept**:
	-  Is the chosen dataset interesting?
	-  **How well does your chosen task fit the chosen dataset**?
	-  Is the task **well formulated**?
	-  Is your task **creative**, did you "think outside the box"?
	-  How **challenging** is the chosen task, did you "make it easy" for yourself?
	-  How well did you use **markdown** to structure and  document your Concept?
2. **15 points: quality of your implementation**:
	-  Was the dataset **imported correctly**?
	-  Did you make sure, that the dataset was **properly cleaned**?
	-  Was your task successfully implemented?
	-  We value either primarily **cleanliness** or **appropriate complexity**, depending on your chosen task.
		- If you choose a rather **simple application**, that you can fulfil with your knowledge from the programming and DIS08 lectures, we want you to produce clean, efficient, and correct code.
		- If you choose a **complex application**, that needs the implementation of more complex coding, we do not value cleanliness and correctness as much. It is ok, if you take parts of code from the web. However, **always make it clear when code is taken from somewhere**, and **make it very clear, where you got it from**!

You do not necessarily lose points, if your results are not exciting, if your concept and implementation are done well. However, **we will punish any forms or attempts of cheating and lacking indication of references severely** (for example, copying from each other, copying parts of work or concepts from other publications without giving credits). Also: Remember, that detailed documentation of your concept and the use of markdown are essential for your rating in the *Concept* category.

Your final points will be calculated as

$$score=concept\times10+implementation\times15$$

where $concept$ and $implementation$ are percentages based on the criteria mentioned above. You will get a percentage score for both criteria and the final grading. The table below illustrates, how some combinations of percentages result in points. As you can see, you can get  a decent amount of points, without implementation, so do not be afraid, if your programming skills are "not amazing"!

| |                       |  |  |  |  |
|------------------------|---------------------------|----|----|----|----|
| Concept: 100% | 10                        | 13.75 | 17.5 | 21.25 | 25 |
|   Concept: 75%                     | 7.5                         | 11.25 | 15 | 18.75 | 22.5 |
|   Concept: 50%                     | 5                         | 8,75  | 12.5 | 16.25 | 20 |
|   Concept: 25%                     | 2.5                         | 6.25  | 10  | 13.75 | 17.5 |
|   Concept: 0%                     | 0                         | 3.75  | 7.5  | 11.25  | 15 |
|                        | Implementation: 0% | Implementation: 25%   |   Implementation: 50% | Implementation: 75%   |Implementation: 100%    |

## Example Concept
To illustrate the task even better, here is an example for a concept (from the L02 hands-on!). **We expect your submissions to be in much more detail**, but you will get a feeling for the types of tasks you could conceptualise and solve.

### Dataset  
|Dataset  | URL | Description |Format |
|--|--|--|--|
| BaumCloud: Dataset on communal trees | [link](https://www.govdata.de/web/guest/suchen/-/details/harmonisierter-datensatz-aus-verschiedenen-kommunalen-baumkatastern) | Many municipalities, counties, and property managers maintain digital tree inventories to manage their tree populations. Some of these stakeholders have released their data as open data to the public. However, this data is available in different places and structured differently. BaumCloud provides a centralised collection and unification of digital tree data. These data are available to the public and can be used e.g. for scientific evaluations, studies or web applications.  | The dataset is available as a .json file (±750mb). Variables: "id", "genus", "species", "name_botanic", "trunk_circum", "treetop_diam", "tree_height", "year_of_planting", "geometry": ("type", "coordinates") |

### Concepts
To illustrate different possible concepts on varying levels of complexity, we give you a two concepts in this example:

#### more comples: Using the BaumCloud dataset, we visualise the most poplar trees for each Bundesland (federated state) as pie charts.
This allows to judge, what types of trees grow best/traditionally in what parts of Germany, for example to select a tree for your garden or street, if you are a local community planer. This task can be implemented using relatively simple python approaches (f.e., exclusively using Pandas). However: you need to find a way, to find the Bundesland for the corresponding coordinates of the trees.

#### complex: Implementation of a tool, that allows selecting a type of tree and showing the nearest trees of that type based on a geo location or show all trees of selected categories (e.g., fruits) in a certain radius.
This more complex implementation leverages python geo-modules such as geoPandas to give a service similar to [mundraub.org](https://mundraub.org/).





