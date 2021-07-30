FROM --platform=linux/amd64 condaforge/mambaforge:latest

RUN mamba install seaborn scikit-learn statsmodels numba pytables
RUN mamba install -c conda-forge python-igraph leidenalg
RUN pip install scanpy
RUN mamba install -c bioconda scrublet
