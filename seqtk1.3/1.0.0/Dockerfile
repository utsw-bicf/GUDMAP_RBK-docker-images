FROM gudmaprbk/seqtk1.3:1.0.0
LABEL author="Gervaise H. Henry"

RUN git clone https://github.com/lh3/seqtk.git && \
  cd seqtk && \
  git checkout v1.3&& \
  make

ENV PATH="/seqtk/:${PATH}"
