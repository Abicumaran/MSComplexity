# MSComplexity

The repository contains our results and raw data used from the Marshall et al. (2021) paper on molecular assembly (MA) algorithm. 

Tha Raw Data folder contains the distance matrix files from the mass spectra of the various molecules Marshall et al. computed the MA indices of, in their figures 2-4. It also contains the 2D-BDM calculations performed on the more complex biological extracts shown in their figure 4.

The Results folder contains all our computations, and excel files with the graphs and the way they were plotted on reproducing the results from all four figures (Fig. 1-4) of the Marshall et al. (2021) paper, with our algorithmic complexity measures.

Marshall, S.M., Mathis, C., Carrick, E. et al. Identifying molecules as biosignatures with assembly theory and mass spectrometry. Nat Commun 12, 3033 (2021). https://doi.org/10.1038/s41467-021-23258-x
To assess the complexity of the biosignatures of biochemical interactome of cell systems these authors (Marshall et al., 2021) used MA algorithm. According to MA model: Model the assembly process as a random walk with weighted trees: The path length of the most likely (probable) structure conformation will reduce in path length (distance matrix). 'The shortest number of steps on a path from the base of the tree to the end of the branch corresponds to the MA of that compound'. We show that this is analogous to compression algorithms within the algorithmic information dynamics (AID) framework. According to the molecular assembly (MA) algorithm: molecules with high MA are very unlikely to form abiotically, and the probability of abiotic formation goes down as MA increases. We used their original datafiles from each of the published figures in Marshall et al. (2021), including the MS/MS data to assess structural heterogeneity of molecules using algorithmic complexity measures. Marshall et al. claimed that  high MA molecules will generate MS2 spectra with many distinct peaks, and that lower MA molecules would generate proportionally fewer since they tend to have fewer bonds and more symmetry. However, we show that their method is sub-optimal to algorithmic complexity estimates.

Our objective: Assess the molecular K-complexity on the various structures using various AID measures. To identify molecular processes characteristic to the emergence of life and identify biological molecules in unknown complex samples. Our BDM (K-complexity estimates) was assessed using the OACC calculator found in:

https://github.com/algorithmicnaturelab/OACC 

1)	Compute BDM, compression length (gzip, LZW, Huffman coding, RLE) on InChI strings
2)	Repeat these measures on the mass spectrometry MS distance matrix of the .mol file for each molecule using the 2D array BDM calculator (binarize at different thresholds)

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
