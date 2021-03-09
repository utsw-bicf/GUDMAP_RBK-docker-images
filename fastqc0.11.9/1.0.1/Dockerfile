FROM gudmaprbk/python3:1.0.1
LABEL author="Gervaise H. Henry"

RUN apt-get update --fix-missing -y && \
  apt-get install -y default-jre

RUN conda install -c bioconda fastqc=0.11.9