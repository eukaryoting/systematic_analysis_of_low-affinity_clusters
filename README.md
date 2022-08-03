# Software used for processing, analysis, and plotting of data from:
### <i> Systematic analysis of low-affinity transcription factor binding site clusters in vitro and in vivo establishes their functional relevance </i>
## https://www.biorxiv.org/content/10.1101/2021.12.17.473130v1
------
Required dependencies can be found in the Requirements.txt file.

## There are four jupyter notebooks:
### in-vivo-analysis_Zif268-Pho4.ipynb
Contains scripts used for the <i>in vivo</i> analysis. 
It can be run independently of the other three notebooks. 

### in-vitro-analysis_Zif268.ipynb
Contains scripts used for the <i>in vitro</i> analysis of Zif268 data. 
For the section that relates gene expression to mean occupancy, it requires 
data generated from the in-vivo-analysis_Zif268-Pho4.ipynb notebook.

### in-vitro-analysis_Pho4.ipynb
Contains scripts used for the <i>in vitro</i> analysis of Pho4 data. 
It can be run independently of the other three notebooks. 

### in-vitro-summary-plotting_Zif268-Pho4.ipynb 
Contains scripts and plotting functionality to generate summary plots
used in the manuscript, for both Zif268 and Pho4 data.
Accordingly, the Zif268 and Pho4 in-vitro-analysis notebooks should be run first.

--------
<b><i>Jupyter notebook cells can be run simply from start to finish (recommended to use Jupyter Lab, and it's possible to run them in the order that they are listed above).</i></b>

<i>There is virtually no install time required.</i>

<i>Raw data is available in this project, and some intermediate data is
also available directly, so that most plotting scripts can be run and plots 
visualized by the user without having to re-run Markov Chain Monte Carlo (MCMC). 
Running MCMC is the most time consuming and computationally intensive section 
of the code. Running MCMC with 10,000 steps will generally take a few hours. 
Due to these steps, running the full code with all of the different models 
will take roughly a full day. </i>

<i>The expected output from the code is generally explained with the detailed
    headers (markdown cells) found throughout the code.</i>
    
    
-------

### Binding site information:
All <i>in vitro</i> DNA targets are 90bp in length.
#### Pho4
"X" stands for non-specific DNA designed not to bind to transcription factor.<br>
"S" represents a strong binding site.<br>
"M" represents a weak binding site.<br>
"W" represents a very-weak binding site.<br>
Ex: M1, M2, M3, are different members of the weak class of binding sites. <br>
Two different notations are used.  Either all non-primer regions are specified: <br>
Ex: S1XXXX represents the DNA target with only the single consensus binding<br>
site in the position furthest from the chip's surface. With remaining DNA designed
to be non-binding to TF.<br>
Or in brackets notation, (gap distance) is specified, corresponding to non-specific<br>
basepairs.

#### Zif268
"A" represents a binding site, without referring to its affinity class. <br>
A11 represents the consensus, strong binding site. <br>
(The S naming is not used for Zif268)<br>
Everything else is similar to Pho4, however with the additional convention <br>
that negative gap distances can be specified for binding sites that share <br>
common basepairs (similar to $\Delta$) in the manuscript. <br>
Ex: A11(-3)A11 refers to two neighbring consensus binding sites that share<br>
three basepairs in common (overlapping)