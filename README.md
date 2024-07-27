# About the Project
This project uses a dataset about the bacteria cultures found within bellybuttons.  
It provides the user with an interactive dashboard containing visualizations about the data.  
A user can select which unique ID should be represented in the visualizations and, upon doing so, the page will populate with:
1. a bar chart outlining the top 10 bacteria cultures found.
2. a bubble chart showing each bacteria culture found scaled by the sample amount found.
3. an info panel containing the metadata about the entry.

The charts are handled in a function buildCHarts(sample).  
This function makes a request for the dataset and then filters it for the specified ID number.  
Then, it extracts the OTU labels, OTU labels, and sample values.  
A bubble chart is created from those variables using Plotly.  

Afterwards, the barchart trace is created using modified versions of the variables above.  
Each list is reversed and sliced so that the top 10 results are represented in the list.  
Then, the barchart is created using those variables with Plotly.  

The info panel is handled by the function buildMetadata(sample).  
This function makes a request for the dataset and then filters it for the specified ID number.  
This metadata is then processed into a list.  
I clear any previous information in the panel using D3's .html() and then I loop through the list and append each key-value pair in a new p tag.  

The above functions are run upon initializing the page using the init() function.
And those functions are also called upon selecting a new option via the optionChanged(newSample) function.

# Built In
Javascript.  
HTML.  

# How to Use
Navigate to the following URL in a browser: https://bramsunner.github.io/da-belly-button-challenge/submission/index.html  
This will allow you to use the site to navigate the dataset.
There is a selector to view all of the separate IDs summaries.

# Resources
Dataset used:  
https://robdunnlab.com/projects/belly-button-biodiversity/  
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0047712  

Bootswatch theme:  
https://bootswatch.com/solar/  
