

An example of file organization to present visualizations for the ENTER project 


![File Organization Diagram](https://github.com/EmoryHPC/practical-data-science/blob/main/file-organization/images/org3.png?raw=true)


Another logical possibility is that we put the "Clustered Heatmaps" and the "Full Length" 

Have as shallow of a hierarchy as possible, that way: 
* Everything can be seen (like going on vacation and leaving your stuff out)
* Don't have snaking file paths
* Don't run into the issue where file path names seem to negate one-another. Let's say I had one apple and I needed to put it in a bucket. Which would I choose: "red objects" or "Fruits"? Sometimes when we create too granular of file names the same issue happens, especially when the objects I want to classify don't have a singular purpose. For instance, say I had a folder named "Congress Article 2025" and a folder named "Canonical Visualizations" for visualizations that I use everywhere. I have a visualization that I use everywhere and put in the Congress article. Is this an effective directory naming scheme? To me the answer could be no, or it could be that I should make a copy of the visualization and put it in both folders. On HPC I can do that with a symlink (or a symbolic link). 
