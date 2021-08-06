FROM --platform=linux/amd64 condaforge/mambaforge:latest

RUN apt-get update
RUN apt-get -y install libhdf5-dev

RUN mamba install seaborn scikit-learn statsmodels numba pytables
RUN mamba install -c conda-forge python-igraph leidenalg
RUN pip install scanpy
RUN mamba install -c bioconda scvi-tools
RUN mamba install -c conda-forge r-base

RUN R -e "install.packages(c('Seurat', 'SeuratObject', 'tidyverse', 'BiocManager', 'harmony', 'future', 'reticulate', 'devtools'), repos = 'http://cran.us.r-project.org')"
RUN R -e "BiocManager::install('ComplexHeatmap')"
RUN R -e "devtools::install_github('mojaveazure/seurat-disk')"
RUN R -e "devtools::install_github('sqjin/CellChat')"

