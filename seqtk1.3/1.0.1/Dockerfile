FROM gudmaprbk/gudmap-rbk_base:1.0.1
LABEL author="Gervaise H. Henry"

RUN apt-get install -y libz-dev

RUN git clone https://github.com/lh3/seqtk.git && \
  cd seqtk && \
  git checkout v1.3&& \
  make

ENV PATH="/seqtk/:${PATH}"