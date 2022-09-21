FROM dokken/ubuntu-20.04

RUN wget https://github.com/graalvm/graalvm-ce-builds/releases/download/vm-22.2.0/graalvm-ce-java17-linux-amd64-22.2.0.tar.gz && \
    tar -xvzf graalvm-ce-java17-linux-amd64-22.2.0.tar.gz && \
    mkdir -p /usr/lib/jvm/ && \
    mv graalvm-ce-java17-22.2.0/ /usr/lib/jvm/graalvm-ce-java17-22.2.0 && \
    cd /usr/lib/jvm/graalvm-ce-java17-22.2.0/bin && \
    export JAVA_HOME=/usr/lib/jvm/graalvm-ce-java17-22.2.0 && \
    export PATH=$JAVA_HOME/bin:$PATH && \
    gu install native-image && \
    sudo apt-get -y install libz-dev && \
    sudo apt-get -y update && sudo apt-get upgrade && \
    sudo apt-get -y install build-essential && \
    sudo apt-get -y install aptitude && \
    sudo apt-get -y install libstdc++6

ENV JAVA_HOME=/usr/lib/jvm/graalvm-ce-java17-22.2.0
ENV PATH=$JAVA_HOME/bin:$PATH