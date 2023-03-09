# About

This is supplementary material for the paper "Revisiting the relevance of traditional genres: a network analysis of fiction readers' preferences."

The larger files in this repository as missing -- I'm waiting to receive more github large data storage. They should be up in about a month. In the meantime, the full supplementary materials can be found at the following link.

https://drive.google.com/file/d/1aFLypkY6rscz4t-ILud-wa4YFn3lXxol/view?usp=sharing

# File Structure

This lists the various files. We organize it folder/subfolder, which are denoted by headings.

## Network Construction Code

This folder contains the code to gather data from goodreads and transform it into a network. 

* *Book Network Analysis.ipynb* -- A Jupyter notebook which gathers the Goodread data and creates the other files.

* *subjects.csv* -- Every book along with what subjects it is listed under.

* *subject counts.csv* -- The number of times each subject appears in subjects.csv

* *subjects_reduced.csv* -- subjects.csv but with every subject that appears less than or equal to twelve times.

* *full_data* -- The same as subjects_reduced but with columns at the end giving the title of the book and which modularity class (community) it is in. Comes in reader and enjoyment versions, and in csv and excel formats.


* *images* -- Folder of images for the Jupyter notebook.



## Networks

This folder contains the outputted networks as Gephi files

* *Enjoyment Network Full* -- The completed enjoyment network. This also includes a breakdown of each subcommunity.

* *Reader Network Full* -- The completed reader network. Also includes a breakdown of each subcommunity. 

### Raw Networks

This folder holds networks that are processed into the final networks.

* *bgraph reader 100k.gml* -- The reader bipartite network: books linked to their readers. 

* *bgraph enjoyment 100k* -- The enjoyment bipartite network: books linked to their readers with ratings less than four filtered out.

* *pgraph 100k reader 10deg.gml* -- The projected version of the reader bipartite network. 

* *pgraph 100k enjoyment 10deg.gml* -- The projected version of the enjoyment network.

### Alternative Networks

This folder contains the finished enjoyment networks when the modularity algorithm split them into five or seven communities (compared to the six that we analyzed in the paper).

## PCA Code

This folder contains code and data for the PCA analysis. Communities are often labeled by an arbitrary number here. Below is a key for the enjoyment network.

|Enjoyment Community  | Number  |
|--|--|
| Thriller | 0 | 
| Fantasy/Scifi | 1|
| Manga | 2 |
| (Modern) Classics | 3  |
| Children's | 4 |
| Contemporary/Realistic | 5 |
| Young Adult | 6 | 

Likewise here is a key for the reader network.

|Reader Community  | Number  |
|--|--|
| Children's | 0 | 
| (Modern) Classics | 1|
| Genre Fiction| 2 |
| Contemporary/Realistic | 3  |
| Young Adult| 4 |
| In Death Series | 5 |

* *PCA and tables* -- Rmd file to run the PCA analysis

### Raw Data

Various .csv files with data used in either the PCA analysis or creating figures in the text. In the enjoyment and reader subcommunities folder there are statistics for each node when restricted to just that subcommunity. 

When a file references a certain number of communities it means the stats were calculated for a network broken down into that number of communities.

### Processed 

Tables of each book sorted by eigencentrality or degree. In the enjoyment and reader subcommunities folder there are the same kind of data for each node when restricted to just that subcommunity. 

When a file references a certain number of communities it means the stats were calculated for a network broken down into that number of communities.
