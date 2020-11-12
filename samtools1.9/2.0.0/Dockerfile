FROM bicf/python3.7:2.0.2
LABEL author="Jon Gesell"

RUN apt-get install -y autoconf automake curl perl zlib1g-dev libbz2-dev liblzma-dev libcurl4-gnutls-dev libssl-dev libncurses5-dev

RUN conda install sambamba && \
    conda update sambamba

RUN wget https://github.com/samtools/samtools/releases/download/1.9/samtools-1.9.tar.bz2 && \
    tar -xvjf samtools-1.9.tar.bz2 && \
    rm samtools-1.9.tar.bz2
WORKDIR /usr/bin//samtools-1.9
RUN ./configure
RUN make && make install
WORKDIR /usr/bin

ENV PATH="/usr/bin/samtools-1.9/bin:$PATH"