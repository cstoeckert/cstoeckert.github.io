Transcription Element Search System: Partial Weight Matrices (tessWms) 
===========================================================================
This program reads (selected) PWMs from a file and predicts binding sites on DNA sequences read from another file.  Hits that have a good enough score are reported in one of four different formats (see usage below).

Installation
===========================================================================
As implemented, the program is fairly simple and has a limited set of requirements to preserve good performance and maintainability across multiple platforms.  Beyond the presence of a C compiler, there should be no dependencies.

To compile executable, simply run:
make tessWms

Usage Example
===========================================================================

tessWms -seq mysequences.fasta -mat mypwms.txt -out my_results.txt -fmt t -mlo 8.0

Usage
===========================================================================
Usage can be printed by executing tessWms without any options, i.e.:

tessWms

This will print the following list of options that can be provided to tessWms:

 -seq string : FASTA file with one or more sequences
               default is -, i.e., stdin.
 -mat string : integer matrix file this is the file that contains the PWM
               * required *
 -out string : write output to this file.
               default is -, i.e., stdout.
 -pat string : only process matrices that contain this string in the defline.
               default is all PWMs.
 -id  string : only process matrices that have this ID (first word on defline.)
               default is all PWMs.
 -mlo float  : only report hits with a log-odds score better than this
               default is 6.0.
 -mxd float  : only report hits with a log-odd score not more that this amount less than best possible score for PWM
               default is 100.0
 -beg int    : report hits 3' of this 1-based position
               default is all positions.
 -end int    : report hits 5' of this 1-based position
               default is all positions.
 -nrc        : do not consider reverse complement strand
               default is both orientations.
 -nno        : do not normalize counts to make probabilities if your PWM is already represented as frequencies, need to use this flag
               default is to compute probabilities
 -tpc float  : total pseudocounts added to counts when computing log-odd scores; negative is sqrt(n)
               default is 1.0.
 -lob p x 4  : probabilities of each base for log-odds calculation I think this is a comma separated list
               default is uniform
 -usb        : use sequence composition as background
               default is use uniform or -lob
 -po  int    : add this amount to reported positions
               default is 0.
 -abt char   : ambiguous base treatment: a (average), o (optimistic), p (pessimistic), or n (none)
               default is pessimistic.
 -fmt char   : output format: b (bulk), t (tab), g (GFF), r (ResultSet-XML), w (WMS-XML). bulk is comma delimitated with very little info; tab a bit more informative output; WMS-XML has most information
               default is WMS-XML.
 -so         : segment the output at each sequence.
               default is no segmentation.
 -q          : remain silent expect to report results.
               default is not to be silent and to report progress on stderr.

PWM Input File Format
===========================================================================
Weight matrices should be provided in the following format. The columns are observations for A, C, G, and T in that order. The rows can be either counts, normalized counts, or probabilities. A file may list one or more matrices.

> PWM_1 defline
1      2      2      0
2      1      2      0
3      0      1      1
0      5      0      0
5      0      0      0
> PWM_2 defline
0      0      4      1
0      1      4      0
0      0      0      5
0      0      5      0
0      1      2      2
0      2      0      3
1      0      3      1

