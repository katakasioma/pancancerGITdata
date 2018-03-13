# pancancerGITdata
1. PPIN was downloaded from [BioGRID](https://thebiogrid.org/download.php) and filtered using [Uniprot](http://www.uniprot.org/) reviewed identifiers (uniprot-all.tab) to obtain BiogridPPIfinal_express. We also used protein abundance data from [PaxDb](http://pax-db.org/species/9606/H.%20sapiens) and [Human Proteome Map](http://www.humanproteomemap.org/) to filter our PPIN and obtain an abundance filtered PPIN (AbundancefilteredBiogridPPI).

2. Paired tumor non-tumor data can be obtained from open access TCGA data <https://gdac.broadinstitute.org/> and <https://portal.gdc.cancer.gov/legacy-archive/search/f>.

3. The R package Xseq (https://cran.r-project.org/web/packages/xseq/vignettes/xseq-package.pdf) was used to detect highly-expressed genes based on mixture-of-Gauassian-distributions For each plot, the left blue curve represents the lowly-expressed genes while the grey curve represents the highly-expressed genes across patients of a cancer type for both healthy and cancer samples, respectively [Supplementary File 1] (https://doc-2c-bg-drive-data-export.googleusercontent.com/download/7oj2q6v2ogmk1u1tr7bisk2uvctatt10/j2oq5vtqn4oeddq4jphd0l131p7rs3s4/1520928000000/da4abce5-3219-49b9-864f-7ff64695b527/109436875571353092805/ADt3v-PTaPDgcOWgIVsOGj_Sp0o2lzJj85zkkO2ofAmCyHcTrog31qfGMX-eHWExbOIm3oKtms88I9yoRbI4UjYtRznrgG1Agwn_0zgFUwZyT7CG_kQk_PgOicbfqeB7Vz_I9ehpQ1QCFNs64ltLuieMrJqjT-6mQtFZ3l8zgZtCAQVxlSDfEYwRXMGPNO_yyiLFF_TnOR9W9EDzGMrB-GCl_EDeZhuZFXxQ0T5VCk5rX6KCJbLtMdtASyr3I4VWRLCXIyhXx1c9qtw-mvqCpLMI-wHqRIkVFcSRSbmDC9oMDTQapnK0XzP1xo0gf_JQZCwexwlbSRM2hLi-NhKL7CXsDCWM2rmHycgEBouVpEVqC_bVHaVCsHpBHfm2kegc09ui2wHERqiC?nonce=0rjcn4qoh8ii6&user=109436875571353092805&authuser=0&hash=fpgrnbp3edto24q6bdeisnp2rkq6h21b).

4. [PPIXpress](https://sourceforge.net/projects/ppixpress/) was used to generate patient specific PPIN using bash command: 

```bashscript
'for i in $(ls TCGA*); do java -jar /home/users/e.kataka/PPIXpress_1.19/PPIXpress_1.19/PPIXpress.jar  -m  -t=0.1  /home/users/e.kataka/CancerPairedData/BiogridPPIfinal_express  out_$i/$i ; done'
```
5. Patient specific perturbation profiles were merged together to obtain cancer type perturbation profiles [Supplementary-Tables-1-13](https://drive.google.com/open?id=0Bz3WS2e_jQ6xU09NN19TWTJVSmM).

6. Perturbed edges occuring in at least two cancer types were all merged to obtain pan-cancer gain and loss profiles (Supplementary Tables 14-15).

7. AbundancefilteredBiogridPPI generated reproducible perturbed edges across the 13 cancer types just like those from BiogridPPIfinal_express. [Supplementary-Tables-1-13-EXTRA](https://drive.google.com/open?id=0Bz3WS2e_jQ6xYnJKdHBUaFVrQ3M).

8. SMGs involved in edgetic perturbations in each cancer are listed in SMGs_driving_perturbations.xlxs (Supplementary Table 16). 
