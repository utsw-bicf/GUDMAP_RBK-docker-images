FROM gudmaprbk/java15:1.0.0
LABEL author="Gervaise H. Henry"

RUN git clone https://github.com/broadinstitute/picard.git && \
  cd picard && \
  git checkout 2.23.9 && \
  echo "distributionBase=GRADLE_USER_HOME" > ./gradle/wrapper/gradle-wrapper.properties && \
  echo "distributionPath=wrapper/dists" >> ./gradle/wrapper/gradle-wrapper.properties && \
  echo "distributionUrl=https\://services.gradle.org/distributions/gradle-6.7-bin.zip" >> ./gradle/wrapper/gradle-wrapper.properties && \
  echo "zipStoreBase=GRADLE_USER_HOME" >> ./gradle/wrapper/gradle-wrapper.properties && \
  echo "zipStorePath=wrapper/dists" >> ./gradle/wrapper/gradle-wrapper.properties && \
  ./gradlew clean build && \
  ./gradlew shadowJar

ENV PATH="/picard/build/libs/:${PATH}"

RUN apt-get install -y autoconf automake curl perl zlib1g-dev libbz2-dev liblzma-dev libcurl4-gnutls-dev libssl-dev libncurses5-dev

WORKDIR /usr/bin
RUN wget https://github.com/samtools/htslib/releases/download/1.11/htslib-1.11.tar.bz2 && \
    tar -vxjf htslib-1.11.tar.bz2 && \
    rm htslib-1.11.tar.bz2
WORKDIR /usr/bin/htslib-1.11
RUN make && make install
WORKDIR /usr/bin

RUN wget https://github.com/samtools/samtools/releases/download/1.11/samtools-1.11.tar.bz2 && \
    tar -xvjf samtools-1.11.tar.bz2 && \
    rm samtools-1.11.tar.bz2
WORKDIR /usr/bin//samtools-1.11
RUN ./configure && \
    make && make install
WORKDIR /usr/bin

ENV PATH="/usr/bin/htslib-1.9/bin:/usr/bin/samtools-1.11/bin:$PATH"