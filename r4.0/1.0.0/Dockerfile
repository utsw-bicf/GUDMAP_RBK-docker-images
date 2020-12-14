FROM gudmaprbk/gudmap-rbk_base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get update -y --fix-missing && \
  apt-get install apt-transport-https software-properties-common gnupg gnupg2 gnupg1 -y && \
  add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu focal-cran40/' && \
  apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9 && \
  apt update -y --fix-missing && \
  apt-get install -y r-base-core r-recommended
  apt-get install -y r-base=4.0.3-1.2004.0 

#Install necessary R packages
RUN R -e "install.packages c((\"BiocManager\",\"optparse\"))" && \
  R -e "BiocManager::install(c(\"DESeq2\", \"edgeR\"))"
