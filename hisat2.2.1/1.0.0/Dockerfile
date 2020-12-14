FROM gudmaprbk/samtools1.11:1.0.0
LABEL author="Jon Gesell"

RUN wget https://cloud.biohpc.swmed.edu/index.php/s/fE9QCsX3NH4QwBi/download && \
  unzip download && \
  rm download && \
  cd hisat2-2.2.1 && \
  make && \
  cd /usr/bin && \
  wget -c http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/gtfToGenePred && \
  wget -c http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/genePredToBed && \
  chmod 755 gtfToGenePred genePredToBed

ENV PATH=/usr/bin/hisat2-2.2.1:/usr/bin/gtfToGenePred:/usr/bin/genePredToBed:${PATH}