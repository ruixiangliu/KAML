# KAMBLUP [![](https://img.shields.io/badge/Issues-1%2B-brightgreen.svg)](https://github.com/YinLiLin/R-KAMBLUP/issues) [![](https://img.shields.io/badge/Release-v1.0.1-blue.svg)](https://github.com/YinLiLin/R-KAMBLUP/commits/master)

## Kinship Adjusted Multi-locus Best Linear Unbiased Prediction

## Contents
* [Getting started](#getting-started)
  - [Installation](#installation)
* [INPUT](#input)
  - [Phenotype file](#phenotype-file)/[Covariate file](#covariate-file)/[Kinship file](#kinship-file)
  - [Genotype file](#genotype-file)
* [USAGE](#usage)
* [OUTPUT](#output)
* [FAQ and Hints](#faq-and-hints)
* [Connect](#connect)

## Getting started
`KAMBLUP` is compatible with both [R](https://www.r-project.org/) and [Microsoft R Open](https://mran.microsoft.com/open/), We highly recommend **MRO** instead of **R** for running `KAMBLUP`. **MRO** is the enhanced distribution of **R**, it includes multi-threaded math libraries. These libraries make it possible for so many common R operations, ***such as matrix multiply/inverse, matrix decomposition, and some higher-level matrix operations***, to compute in parallel and use all of the processing power available to [reduce computation times](https://mran.microsoft.com/documents/rro/multithread/#mt-bench).

### Installation
`KAMBLUP` is not available on CRAN, but can be installed using the R package **"devtools"**. There are two packages should be installed beforehand, **"snpStats"** and **"rfunctions"**. `KAMBLUP` can be installed with the following R code:
```r
#if "devtools" isn't installed, please "install.packages(devtools)" first.
devtools::install_github("Bioconductor-mirror/snpStats")
devtools::install_github("jaredhuling/rfunctions")
devtools::install_github("YinLiLin/R-KAMBLUP/")
```

## INPUT
### Phenotype file
> `test.txt`

| Trait1 | Trait2 | Trait3 |
| :---: | :---: |  :---: |
| 3.20 | NA | 1 |
| 0.58 | 58.2 | NA|
| NA | 35.7 | 0 |
| -0.25 | 42.4 | 1|
| NA | NA | 0|

### Covariate file
> `testCV.txt`

### Kinship file
> `testKin.txt`

### Genotype file
> `test.geno.desc, test.geno.bin`
```r
KAMBLUP.Data(hfile="", out="test")
```
```r
KAMBLUP.Data(bfile="", out="test")
```
```r
KAMBLUP.Data(numfile="", mapfile="", out="test")
```

## USAGE
```r
KAMBLUP(pfile="./test.txt", pheno=1, gfile="./test")
```
```r
KAMBLUP(pfile="./test.txt", pheno=1, gfile="./test", cfile="./testCV.txt", kfile="./testKin.txt")
```

## OUTPUT

## FAQ and Hints :arrow_right:

## Contact
Questions, suggestions, and bug reports are welcome and appreciated.
- **Author:** Lilin Yin<ylilin@163.com>
- **Institution:** [*Huazhong agricultural university*](http://www.hzau.edu.cn/2014/ch/)
