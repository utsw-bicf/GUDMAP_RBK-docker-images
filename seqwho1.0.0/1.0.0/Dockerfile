FROM gudmaprbk/python3:1.0.0
LABEL author="Gervaise H. Henry"

RUN pip3 install Cython==0.29.21
RUN pip3 install joblib==1.0.1 seaborn==0.11.1 more-itertools==8.7.0 scikit-learn==0.21.3 && \
    git clone --depth 1 --branch v1.0.0 https://github.com/DaehwanKimLab/seqwho.git /seqwho
ENV PATH=/seqwho:$PATH

RUN apt-get install -y libz-dev
RUN git clone https://github.com/lh3/seqtk.git && \
  cd seqtk && \
  git checkout v1.3&& \
  make
ENV PATH="/seqtk/:${PATH}"