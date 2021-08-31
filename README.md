### 1. [NoBadWordsCombiner](http://hsdfinder.com/combiner/) 
automatically integrate the gene models annotations (e.g., NCBI, SwissProt, etc.), and minimize those "bad words" (e.g., hypothetical and uncharacterized proteins)

### 2. What's NoBadWordsCombiner?
Unlike the NCBI-NR or UniProtKB/Swiss-Prot, although they provide valuable function description of the interested genes; however, many hypothetical proteins or ‘bad name’ proteins are also included in the respective database, which will mess up the interpretation of functional gene annotations. Although it is not the focus of this article, we have developed another software can integrate the gene function information together minimize ‘bad words’ including Nr-NCBI, UniProtKB/Swiss-Prot, KEGG, and Pfam etc..
```
#Environmental Requirement: Pandas
#To collect pandas packages : 

sudo pip install pandas
python NoBadWordsCombiner.py -h
python NoBadWordsCombiner.py -n <NCBI file> -s <Swiss file> -g <Gene list file> -k <Gene list file with KO annotation> -p <pfam file> -t <type> -o <output file name>

# Or use 
python NoBadWordsCombiner.py --ncbi_file=<NCBI file> --swiss_file=<Swiss file> --gene_file=<Gene list file> --ko_file=<Gene list file with KO annotation> --pfam_file=<pfam file> --type=<type> -output_file=<output file name>
```

### 3.Limitation
There is a possible steep learning curve for users with limited knowledge of bioinformatics, especially for those who are not familiar with the basic BLAST package and dash shell in a Linux/Unix environment. We do hope to further develop the tool, making it more user friendly, including trying to remove some of the middle steps. Unfortunately, we are not yet able to provide a “one-click solution” because of the incompatibility of the various databases employed by the tool. That said, we still believe that our tool is comparatively easier to use than some of the other options currently available to scientists. Indeed, presently there are very few tools that can search eukaryotic genome projects, efficiently merging hits from various databases and strengthening gene definitions by minimizing functional descriptions containing ‘bad words’. Thus, we believe that our tool will provide a well-needed service to the bioinformatics and genomics community.

### 4. Reference
X. Zhang, Yining. Hu, D. Smith (2021). Protocol for using NoBadWordsCombiner to merge and minimize ‘bad words’ from BLAST hits against multiple eukaryotic gene annotation databases etc. doi: upcoming

X. Zhang, et.al. D. Smith (2021). Draft genome sequence of the Antarctic green alga _Chlamydomonas_ sp. UWO241 DOI:https://doi.org/10.1016/j.isci.2021.102084

### 5. Contact
Usage of this site follows AWS’s Privacy Policy. © Copyright (C) 2021
