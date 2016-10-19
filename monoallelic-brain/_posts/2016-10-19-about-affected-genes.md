---
layout: post
---

Based on the aggregation of various p-values from [a previous analysis]({{ site.baseurl }}{% post_url 2016-10-03-permutation-test %}), a list of those genes was collated, which are significantly affected by any of the four chosen coefficients (Age, GenderMale, DxSCZ, Ancestry.1) representing various biological variables (see [signif-gene-effects-either.csv]).  These genes were then queried against Ensemble Genes 86 database, Homo sapiens genes (GRCh38.p7) using BioMart with the following HGNC symbols as input external reference IDs:

MAGEL2,
MIR668,
MEG8,
NAP1L5,
MEG3,
PEG3,
NDN,
PEG10,
KCNQ1OT1,
ZDBF2,
KCNK9,
INPP5F,
MEST,
PWRN1,
UBE3A

Note that in the above list MIR668 replaced AL132709.5 and MEG8 replaced RP11-909M7.3 because the latter IDs used as HGNC symbols gave no hit in Ensemble.

The following attributes were obtained:

Gene type,
Phenotype description,
Study External Reference,
Description,
Associated Gene Name,
Ensembl Family Description,
Chromosome Name,
Gene Start (bp)

The resulting table was saved in [signif-gene-effects-either-biomart.csv][signif-gene-effects-either-biomart.csv].  Those information were extended manually and saved in [signif-gene-effects-either-manual-annot.csv][signif-gene-effects-either-manual-annot.csv].

[signif-gene-effects-either.csv]: {{ site.baseurl }}/assets/projects/monoallelic-brain/signif-gene-effects-either.csv
[signif-gene-effects-either-biomart.csv]: {{ site.baseurl }}/assets/projects/monoallelic-brain/signif-gene-effects-either-biomart.csv
[signif-gene-effects-either-manual-annot.csv]: {{ site.baseurl }}/assets/projects/monoallelic-brain/signif-gene-effects-either-manual-annot.csv