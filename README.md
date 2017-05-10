# pancancerGITdata
1.PPIN was downloaded from [BioGRID](https://thebiogrid.org/download.php) and filtered using [Uniprot](http://www.uniprot.org/) reviewed identifiers (uniprot-all.tab) to obtain BiogridPPIfinal_express.
2.[PPIXpress](https://sourceforge.net/projects/ppixpress/) was used to generate patient specific PPIN. THe bash command ran was: Inline 'for i in $(ls *_{COAD,LUAD,LUSC,HNSC}); do java -jar /home/users/e.kataka/PPIXpress_1.14/PPIXpress_1.14/PPIXpress.jar  -g  -t=0.1  /home/users/e.kataka/CancerPairedData/BiogridPPIfinal_express  outTumor_$i/  $i ;done'
