FROM --platform=linux/amd64 condaforge/mambaforge:latest


RUN mamba install -c conda-forge r-tidyverse r-svglite libiconv mscorefonts
RUN mamba install -c bioconda bioconductor-deseq2=1.32 bioconductor-tximeta=1.10 bioconductor-ihw=1.20 bioconductor-apeglm=1.14
RUN mamba install -c bioconda bioconductor-org.hs.eg.db=3.13




# FROM rocker/r-base:4.1.0
# RUN R -e 'install.packages(c("BiocManager"))'
# RUN R -e 'BiocManager::install(c("DESeq2", "IHW", "tximeta", "apeglm"))'
