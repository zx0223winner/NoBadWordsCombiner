### 1. NoBadWordsCombiner (http://hsdfinder.com/combiner/) 
automatically integrate the gene models annotations (e.g., NCBI, SwissProt, etc.), and minimize those "bad words" (e.g., hypothetical and uncharacterized proteins)

### 2. What's NoBadWordsCombiner?
Unlike the NCBI-NR or UniProtKB/Swiss-Prot, although they provide valuable function description of the interested genes; however, many hypothetical proteins or ‘bad name’ proteins are also included in the respective database, which will mess up the interpretation of HSDs results. Although it is not the focus of this article, we have developed another software can integrate the gene function information together minimize ‘bad words’ including Nr-NCBI, UniProtKB/Swiss-Prot, KEGG, Pfam and GO etc..
```
Environmental Requirement: Pandas
To collect pandas packages : sudo pip install pandas

python NoBadWordsCombiner.py -h

Combiner.py -n <NCBI file> -s <Swiss file> -g <Gene list file> -k <Gene list file with KO annotation> -p <pfam file> -t <type> -o <output file name>
Or use Combiner.py --ncbi_file=<NCBI file> --swiss_file=<Swiss file> --gene_file=<Gene list file> --ko_file=<Gene list file with KO annotation> --pfam_file=<pfam file> --type=<type> -output_file=<output file name>
```

### 3. Reference
X. Zhang, Yining. Hu, D. Smith (2021). NoBadWordsCombiner - NoBadWords Combiner can integrate the gene function information together and minimize ‘bad words’ including Nr-NCBI, UniProtKB/Swiss-Prot, KEGG, Pfam and GO etc. doi: upcoming

X. Zhang, et.al. D. Smith (2021). Draft genome sequence of the Antarctic green alga _Chlamydomonas_ sp. UWO241 DOI:https://doi.org/10.1016/j.isci.2021.102084

### 4. Contact
Usage of this site follows AWS’s Privacy Policy. © Copyright (C) 2021 https://github.com/zx0223winner/NoBadWordsCombiner
