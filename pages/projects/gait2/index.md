---
layout: page
title: The GAIT2 project
---

<!--
<div class="navbar">
    <div class="navbar-inner">
        <ul class="nav">
            <li><a href="#assoc">QTL asssociation mapping</a></li>
        </ul>
    </div>
</div>
-->

### <a name="about"></a>About

In GAIT2, we recruited 935 individuals grouped in 35 pedigrees, 
with on average of 27 individuals per pedigree and a  total of 8654 related pairs. 
All families have at least 10 living individuals in three or more generations, 
and were recruited and  selected as part of a study on idiopathic thrombophilia 
with an age range of 3 to 101 years (mean 40). 
Hundreds of quantitative phenotypes were measured at time of recruitment, 
including anthropometric measurements, hemogram, hemostasis traits, 
as well as phenotypes related with platelets, platelet activity, homocysteine metabolism, 
inflammation, and flow cytometry of leukocytes and microparticles. 
Genotypes obtained from a mix of Illumina 1M and Illumina 500K chips were imputed into a 1000 genomes reference panel. 
We sequenced the mRNA transcriptome from whole blood for all the individuals, at the time of collection not medicated for thrombophilia.

### <a name="assoc"></a>QTL association mapping

Around a hundred traits were mapped using around 10 millions of SNPs.
The ultra-fast score-based GLS method [MatrixeQTL](http://www.bios.unc.edu/research/genomic_software/Matrix_eQTL/)
allowed to efficiently evaluate the association models.

* [Interactive Heatmap]({{ site.baseurl }}/reports/assoc-mapping2/heatmap2.html) _traits vs. SNPs_, MAF >= 0.01, genome-wide significant level < 5e-8
    * [Static Heatmap]({{ site.baseurl }}/reports/assoc-mapping2/static-heatmap1.html) _traits vs. SNPs_, MAF >= 0.01, genome-wide suggestive level < 1e-5 
* [Interactive Scatterplot]({{ site.baseurl }}/reports/assoc-mapping2/scoreplot.html) _h2r vs. #SNPs_, MAF >= 0.01

The results are stored in the private repository of the group [GAIT2](https://github.com/ugcd/GAIT2),
directory [projects/02-assoc-mapping2-matrix](https://github.com/ugcd/GAIT2/tree/master/projects/02-assoc-mapping2-matrix).
Some links of the interest (all to the private group repository): 

* Manhattan plots produced for all traits under study: [link to download PDF](https://github.com/ugcd/GAIT2/raw/master/projects/02-assoc-mapping2-matrix/output/assoc/manhattan.A.maf001.mapping2.gait2.matrix.pdf).
* Directory [output/assoc/](https://github.com/ugcd/GAIT2/tree/master/projects/02-assoc-mapping2-matrix/output/assoc) contains _CSV_ tables of the association results for all the traits.
* Report [reports/01-comparison-F11/01-comparison-F11.md](https://github.com/ugcd/GAIT2/blob/master/projects/02-assoc-mapping2-matrix/reports/01-comparison-F11/01-comparison-F11.md) presents a comparison of GWAS results produced by LMM method and score-based GLS method (used here for QTL asssociation mapping).

_MatrixeQTL_ under GAIT2-specific settings seems to show
consistent results in terms of the _genome-wide_ significant signals,
but the overall tendency is towards overestimation of the p-values.
Thus, the reported signals are needed to be further refined with a more precise approach.
In general, the prioritization of SNPs produced by _MatrixeQTL_ is a good starting point 
to cope with the large-scale problem of QTL mapping.
