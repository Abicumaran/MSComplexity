# MSComplexity

The repository contains our results and raw data used in our critique of the Marshall et al. (2021) paper on molecular assembly (MA) algorithm. 
Our paper entitled "On the Salient Limitations of the Methods of Assembly Theory and their Classification of Molecular Biosignatures" can be found at: DOI: 10.48550/arXiv.2210.00901
https://arxiv.org/abs/2210.00901

Tha Raw Data folder contains the distance matrix files from the various molecules Marshall et al. computed the MA indices of, in their figures 1 and 2 to create the MA chemical space, as well as their InChI strings. It also contains the AID calculations performed on the 114 molecules shown in their Figure 3, and the measures for the 18 (out of 25 molecules disclosed) for more complex biological extracts (mixtures) shown in their figure 4, directly on the peak matrices from their MS2 mass spectrometry data. 

The Results.zip folder contains all the .csv files with the graphs. They are provided so they can be re-plottedby users for reproducing the results from all four figures (Fig. 1-4) of the Marshall et al. (2021) paper, with our algorithmic complexity measures.

Marshall, S.M., Mathis, C., Carrick, E. et al. Identifying molecules as biosignatures with assembly theory and mass spectrometry. Nat Commun 12, 3033 (2021). https://doi.org/10.1038/s41467-021-23258-x

To assess the complexity of the biosignatures of biochemical interactome of cell systems these authors (Marshall et al., 2021) used MA algorithm. According to MA model: Model the assembly process as a random walk with weighted trees: The path length of the most likely (probable) structure conformation will reduce in path length (distance matrix). 'The shortest number of steps on a path from the base of the tree to the end of the branch corresponds to the MA of that compound'. We show that this is analogous to compression algorithms within the algorithmic information dynamics (AID) framework. According to the molecular assembly (MA) algorithm: molecules with high MA are very unlikely to form abiotically, and the probability of abiotic formation goes down as MA increases. We used their original datafiles from each of the published figures, including the MS/MS data to assess structural heterogeneity of molecules using algorithmic complexity measures. Marshall et al. claimed that  high MA molecules will generate MS2 spectra with many distinct peaks, and that lower MA molecules would generate proportionally fewer since they tend to have fewer bonds and more symmetry. However, we show that their method is sub-optimal to pre-existing algorithmic complexity estimates.

Our objective: Assess the molecular K-complexity on the various structures using various AID measures. To identify molecular processes characteristic to the emergence of life and identify biological molecules in unknown complex samples. Our BDM (K-complexity estimates) was assessed using the OACC calculator found in:

https://github.com/algorithmicnaturelab/OACC 

1)	Compute BDM, compression length (LZW, Huffman coding, RLE) on InChI strings
2)	Repeat these measures on the mass spectrometry MS distance matrix of the .mol file for each molecule using the 2D array BDM calculator (binarize at different thresholds)
3)	Perform 2D-BDM on the MS2 mass spectra (peak amtrices) of the biological extracts/mixtures from Figure 4 of Marshall et al.

We have also included the source data files from MA/Assembly theory in the folder ATSourceData.zip.


https://planetcalc.com/9069/

https://www.rapidtables.com/convert/number/ascii-to-binary.html 

We had to covert numeric values to binary by use of different conversion thresholds. 
https://stackoverflow.com/questions/57737386/how-to-convert-numeric-values-to-binary-using-a-threshold-in-r 

2D-BDM Python code:
https://github.com/sztal/pybdm 

HUFFMAN CODE:
https://www.dcode.fr/huffman-tree-compression

SIMPLE RLE:
https://www.techiedelight.com/run-length-encoding-rle-data-compression-algorithm/ 
