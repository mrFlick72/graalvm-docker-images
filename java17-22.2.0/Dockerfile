FROM alpine

RUN wget https://github.com/graalvm/graalvm-ce-builds/releases/download/vm-22.2.0/graalvm-ce-java17-linux-amd64-22.2.0.tar.gz && \
    tar -xvzf graalvm-ce-java17-linux-amd64-22.2.0.tar.gz && \
    mv graalvm-ce-java17-22.2.0/ /usr/lib/jvm/

ENV JAVA_HOME=/usr/lib/jvm/graalvm-ce-java17-22.2.0
ENV PATH=$JAVA_HOME/bin:$PATH