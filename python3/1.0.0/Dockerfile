FROM gudmaprbk/gudmap-rbk_base:1.0.0
LABEL author="Gervaise H. Henry"

RUN apt-get install -y python3 python3-pip

RUN wget http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
  bash Miniconda3-latest-Linux-x86_64.sh -p /miniconda -b && \
  rm Miniconda3-latest-Linux-x86_64.sh
ENV PATH=/miniconda/bin:${PATH}                                                                                      

RUN conda config --add channels defaults && \
  conda config --add channels bioconda && \
  conda config --add channels conda-forge && \
  conda update -n base -c defaults -y conda

RUN pip3 install --upgrade pip

RUN pip3 install argparse==1.4.0 
RUN conda install pandas=0.25.3