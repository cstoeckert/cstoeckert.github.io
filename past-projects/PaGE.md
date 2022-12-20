# Patterns from Gene Expression (PaGE)
PaGE was a free downloadable software for microarray analysis. PaGE can be used to produce sets of differentially expressed genes with confidence measures attached. These lists are generated the False Discovery Rate method of controlling the false positives.

But PaGE is more than a differential expression analysis tool. PaGE is a tool to attach descriptive , dependable, and easily interpretable expression patterns to genes across multiple conditions, each represented by a set of replicated array experiments.

The input consists of (replicated) intensities from a collection of array experiments from two or more conditions (or from a collection of direct comparisons on 2-channel arrays). The output consists of patterns, one for each row identifier in the data file.

One condition is used as a reference to which the other types are compared. The length of a pattern equals the number of non-reference sample types. The symbols in the patterns are integers, where positive integers represent up-regulation as compared to the reference sample type and negative integers represent down-regulation.

The patterns are based on the false discovery rates for each position in the pattern, so that the number of positive and negative symbols that appear in each position of the pattern is as descriptive as the data variability allows.

The patterns generated are easily interpretable in that integers are used to represent different levels of up- or down-regulation as compared to the reference sample type.

## Publications

* Grant G.R., Liu J., Stoeckert C.J.Jr. (2005) A practical false discovery rate approach to identifying patterns of differential expression in microarray data, Bioinformatics, Vol 21 no 11, 2684-2690.

Note: There is a typo in this publication on page 2686 in formula for muk(i+1) (the second to last displayed forumla on the page). On the right hand side, the first muk(i) should be mu-tildek(1) (i replaced by 1).

* Grant G.R., Liu J., Stoeckert C.J.Jr. The technical manual for PaGE 5.1.

* Grant G.R., Manduchi E., Stoeckert C.J. Jr. Using non-parametric methods in the context of multiple testing to identify differentially expressed genes. Methods of microarray data analysis, editors S.M. Lin and K.F. Johnson, Kluwer Academic Publishers (Boston, 2002): 37-55. (Winner of the best presentation award CAMDA'00).

* Manduchi E., Grant G.R., McKenzie S.E., Overton G.C., Surrey S., Stoeckert C.J. Jr. (2000) Generation of patterns from gene expression data by assigning confidence to differentially expressed genes,  Bioinformatics, 16(8): 685-698. 
