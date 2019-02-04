# pancancerGITdata
1. PPIN was downloaded from [BioGRID](https://thebiogrid.org/download.php) and filtered using [Uniprot](http://www.uniprot.org/) reviewed identifiers (uniprot-all.tab) to obtain BiogridPPIfinal_express. We also used protein abundance data from [PaxDb](http://pax-db.org/species/9606/H.%20sapiens) and [Human Proteome Map](http://www.humanproteomemap.org/) to filter our PPIN and obtain an abundance filtered PPIN (AbundancefilteredBiogridPPI).

2. Paired tumor non-tumor data can be obtained from open access TCGA data <https://gdac.broadinstitute.org/> and <https://portal.gdc.cancer.gov/legacy-archive/search/f>.

3. The R package Xseq (https://cran.r-project.org/web/packages/xseq/vignettes/xseq-package.pdf) was used to detect highly-expressed genes based on mixture-of-Gauassian-distributions For each plot, the left blue curve represents the lowly-expressed genes while the grey curve represents the highly-expressed genes across patients of a cancer type for both healthy and cancer samples, respectively [Supplementary File 1](https://drive.google.com/open?id=1ci6TgK7qMl1fKsulgDsaYWVTGCSK0y-e).

4. [PPIXpress](https://sourceforge.net/projects/ppixpress/) was used to generate patient specific PPIN using bash command: 

```bashscript
'for i in $(ls TCGA*); do java -jar /home/users/e.kataka/PPIXpress_1.19/PPIXpress_1.19/PPIXpress.jar  -m  -t=0.1  /home/users/e.kataka/CancerPairedData/BiogridPPIfinal_express  out_$i/$i ; done'
```
5. Patient specific perturbation profiles were merged together to obtain cancer type perturbation profiles [Supplementary-Tables-1-13A](https://drive.google.com/file/d/1SyCRGR1cJGIgl3qqWfRNWnvXo0ry-ocp/view?usp=sharing).

6. AbundancefilteredBiogridPPI generated reproducible perturbed edges across the 13 cancer types just like those from BiogridPPIfinal_express. [Supplementary Tables1-13_EXTRA.xlxs.tar.gz](https://drive.google.com/open?id=1AvUBF5WHf-ackau_gwTa7O1WEGjPodsP).

7. All enriched Ontologies from topGO and REVIGO for the proteins involved in cancer-specific edgetic gains and losses (Supplementary File 2.xlsx).  

8. Uniprot identifiers for the SMGs involved in edgetic perturbations in each cancer and the paired genes based on degree similarity are listed in Supplementary File 3a. Randomly generated genes having substantially more perturbations than SMGs are listed in Supplementary File 3b.

9. Perturbed edges occuring in at least two cancer types were all merged to obtain pan-cancer gain and loss profiles (Supplementary Files 4 & 5). Proteins involved in pan-cancer edgetic perturbations are known cancer biomarkers and affect distinct pathways, Supplementary File 6.

10. Proteins involved in cancer-specific and subtype-specific significant edgetic pertutbations and corresponding survival analysis plots are available in Supplementary Table 7 and Supplementary Figure 3.

11. Edgetic perturbations cut across all stages in cancer; Stages I, II, III and IV, Supplementary File 8.docx.

12. Significantly rewired nodes comprise of known cancer biomarkers and are also involved in multiple diseases, Supplementary File 9.gz.
 
