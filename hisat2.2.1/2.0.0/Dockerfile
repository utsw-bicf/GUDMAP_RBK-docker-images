FROM gudmaprbk/samtools1.9:1.0.0
LABEL author="Jon Gesell"

RUN wget https://cloud.biohpc.swmed.edu/index.php/s/fE9QCsX3NH4QwBi/download && \
  unzip download && \
  rm download && \
  cd hisat2-2.2.1 && \
  make && \
  cd /

ENV PATH=/usr/bin/hisat2-2.2.1:${PATH}