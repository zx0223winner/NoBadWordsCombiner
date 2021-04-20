### NoBadWordsCombiner (http://hsdfinder.com/combiner/) 
automatically merge the gene models annotations (e.g., NCBI, SwissProt, etc.) and screen out those "bad words" (e.g., hypothetical and uncharacterized proteins)

#### What's NoBadWordsCombiner?
Unlike the NCBI-NR or UniProtKB/Swiss-Prot, although they provide valuable function description of the interested genes; however, many hypothetical proteins or ‘bad name’ proteins are also included in the respective database, which will mess up the interpretation of HSDs results. Although it is not the focus of this article, we have developed another software can integrate the gene function information together without ‘bad words’ including Nr-NCBI, UniProtKB/Swiss-Prot, KEGG, Pfam and GO etc..
```
Environmental Requirement: Pandas
To collect pandas packages : sudo pip install pandas

python NoBadWordsCombiner.py -h

Combiner.py -n <NCBI file> -s <Swiss file> -g <Gene list file> -k <Gene list file with KO annotation> -p <pfam file> -t <type> -o <output file name>
Or use Combiner.py --ncbi_file=<NCBI file> --swiss_file=<Swiss file> --gene_file=<Gene list file> --ko_file=<Gene list file with KO annotation> --pfam_file=<pfam file> --type=<type> -output_file=<output file name>
```
========================
NoBadWordsCombiner
========================

.. image:: www.
        :target: www.

Python package for testing 


Ever get?

This should save some headaches later


Requirements
------------
NoBadWordsCombiner requires the following packages be installed:


python >= 3.6.0


It also requires 



Installation
------------
.. code-block:: console

        pip install XXX


Usage
------------
For basic usage, run  Combiner.py -h

.. code-block:: console

       Combiner.py -n <NCBI file> -s <Swiss file> -g <Gene list file> -k <Gene list file with KO annotation> -p <pfam file> -t <type> -o <output file name> Or use Combiner.py --ncbi_file=<NCBI file> --swiss_file=<Swiss file> --gene_file=<Gene list file> --ko_file=<Gene list file with KO annotation> --pfam_file=<pfam file> --type=<type> -output_file=<output file name>


Output
------------
check_strandedness will print to console the results of infer_experiment.py (http://rseqc.sourceforge.net/#infer-experiment-py), along with an interpretation.

.. code-block:: console

        checking strandedness
        Reading reference gene model stranded_test_WT_yeast_rep1_1_val_1_1/Saccharomyces_cerevisiae.R64-1-1.98.bed ... Done
        Loading SAM/BAM file ...  Total 20000 usable reads were sampled
        This is PairEnd Data
        Fraction of reads failed to determine: 0.0595
        Fraction of reads explained by "1++,1--,2+-,2-+": 0.0073 (0.8% of explainable reads)
        Fraction of reads explained by "1+-,1-+,2++,2--": 0.9332 (99.2% of explainable reads)
        Over 90% of reads explained by "1+-,1-+,2++,2--"
        Data is likely RF/fr-firststrand


Any intermediate files are written to a folder in your current working directory derived from the name of the reads_1 file.


How it Works
------------
check_strandedness.py runs a series of commands to check which direction reads align once mapped in transcripts.

It first creates a kallisto index (or uses a pre-made index) of your organisms transcriptome.

It then maps a small subset of reads (default 200000) to the transcriptome, and uses kallisto's --genomebam argument to project pseudoalignments to genome sorted BAM file.

It finally runs RSeQC's infer_experiment.py to check which direction reads from the first and second pairs are aligned in relation to the transcript strand, and provides output with the likely strandedness of your data.
