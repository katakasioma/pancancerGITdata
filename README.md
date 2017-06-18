# pancancerGITdata
1. PPIN was downloaded from [BioGRID](https://thebiogrid.org/download.php) and filtered using [Uniprot](http://www.uniprot.org/) reviewed identifiers (uniprot-all.tab) to obtain BiogridPPIfinal_express. We also used protein abundance data from PaxDb () and HPM() to filter our PPIN and obtain an abundance filtered PPIN ().
2. Paired tumor non-tumor data can be obtained from open access TCGA data <https://gdac.broadinstitute.org/> and <https://portal.gdc.cancer.gov/legacy-archive/search/f>
3. [PPIXpress](https://sourceforge.net/projects/ppixpress/) was used to generate patient specific PPIN using bash command: 

```bashscript
'for i in $(ls TCGA*); do java -jar /home/users/e.kataka/PPIXpress_1.14/PPIXpress_1.14/PPIXpress.jar  -g  -t=0.1  /home/users/e.kataka/CancerPairedData/BiogridPPIfinal_express  out_$i/$i ; done'
```
4. Patient specific perturbatio profiles were merged together to obtain cancer type perturbation profiles ()
5. Strictly gained and strictly lost edges were all merged to obtain pan-cancer gain and loss profiles ()
