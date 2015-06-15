# pScatter

##For visualizing pLink data from one or more experiments

by Justin Jee, with design by Katelyn McGary Shipper

*Dependencies*

pScatter uses [python](https://www.python.org/downloads/), [numpy](http://www.numpy.org/), and the visualization library [matplotlib](http://matplotlib.org/)

*Basic Use*

To download, either download all 3 .py files into the same directory, or download the zipped folder (see button on the bottom right) 

The inputs to pScatter include:

1.   A fasta file including the amino acid sequences of all the proteins under consideration.
2.   A list of amino acids of interest (ex: K or CM)
3.   Up to three directories containing pLink files (in .txt format) with crosslink information (of the form ProteinA(position1)-ProteinB(position2))
Note: If converting from excel to .txt files, it is important to save it in WINDOWS TXT FORMAT. Even if you are on Mac. 
The exact features the program looks for in a given line are in the conditional "if ('Spectrum' in line) and ')-' in line and not ('REVERSE' in line):"
You can modify this in loadfiles.py if your file looks different.

The outputs include:

1.   A summary file (.txt) containing the list of all links and their frequencies
2.   A scatter plot

*Example*

python pScatter.py test.fasta K EXP1 EXP2 testout

*Features*

--scale

Scales both plot and output so that only the amino acids of interest are considered. Axes are in units of amino acids of interest (ex: 1st lysine, 2nd lysine, etc)

--zoom=Prot1-Prot2

Zooms in on only one subplot (Prot1 vs Prot2). As an added feature, clicking on any point in the scatter plot will print the coordinates of that point in the console.

--xkcd

Because why not.
