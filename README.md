### NoBadWordsCombiner (http://hsdfinder.com/combiner/) 
automatically integrate the gene models annotations (e.g., NCBI, SwissProt, etc.), and minimize those "bad words" (e.g., hypothetical and uncharacterized proteins)

#### What's NoBadWordsCombiner?
Unlike the NCBI-NR or UniProtKB/Swiss-Prot, although they provide valuable function description of the interested genes; however, many hypothetical proteins or ‘bad name’ proteins are also included in the respective database, which will mess up the interpretation of HSDs results. Although it is not the focus of this article, we have developed another software can integrate the gene function information together minimize ‘bad words’ including Nr-NCBI, UniProtKB/Swiss-Prot, KEGG, Pfam and GO etc..
```
Environmental Requirement: Pandas
To collect pandas packages : sudo pip install pandas

python NoBadWordsCombiner.py -h

Combiner.py -n <NCBI file> -s <Swiss file> -g <Gene list file> -k <Gene list file with KO annotation> -p <pfam file> -t <type> -o <output file name>
Or use Combiner.py --ncbi_file=<NCBI file> --swiss_file=<Swiss file> --gene_file=<Gene list file> --ko_file=<Gene list file with KO annotation> --pfam_file=<pfam file> --type=<type> -output_file=<output file name>
```

