FROM gudmaprbk/python3:1.0.0
LABEL author="Gervaise H. Henry"

RUN add-apt-repository ppa:openjdk-r/ppa && \
  apt-get update --fix-missing -y && \
  apt-get install -y openjdk-12-jdk-headless

RUN conda install -c bioconda fastqc=0.11.9

ENTRYPOINT ["fastqc"]