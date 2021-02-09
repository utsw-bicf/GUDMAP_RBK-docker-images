FROM gudmaprbk/python3:1.0.0
LABEL author="Gervaise H. Henry"

RUN pip3 install Cython==0.29.21
RUN pip3 install joblib==1.0.1 seaborn==0.11.1 more-itertools==8.7.0 scikit-learn==0.21.3 && \
    git clone https://git.biohpc.swmed.edu/s181649/seqwho.git /seqwho
ENV PATH=/seqwho:$PATH