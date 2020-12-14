FROM gudmaprbk/fastqc0.11.9:1.0.0
LABEL author="Gervaise H. Henry"

RUN pip3 install --upgrade cutadapt==3.1

RUN apt-get install -y curl

RUN curl -fsSL https://github.com/FelixKrueger/TrimGalore/archive/0.6.5.tar.gz -o trim_galore.tar.gz && \
  tar xvzf trim_galore.tar.gz && \
  rm -rf /trim_galore.tar.gz

ENV PATH="/TrimGalore-0.6.5/:${PATH}"