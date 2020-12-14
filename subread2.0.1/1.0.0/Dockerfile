FROM gudmaprbk/r4.0:1.0.0
LABEL author="Gervaise H. Henry"

RUN wget "https://downloads.sourceforge.net/project/subread/subread-2.0.1/subread-2.0.1-source.tar.gz" && \
  tar -xvzf subread-2.0.1-source.tar.gz && \
  rm subread-2.0.1-source.tar.gz && \
  cd /subread-2.0.1-source/src && \
  make -f Makefile.Linux && \
  cd /

ENV PATH="/subread-2.0.1-source/bin:${PATH}"
