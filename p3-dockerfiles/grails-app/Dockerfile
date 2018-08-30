FROM ubuntu AS grail-env

ENV javaVersion 8.0.181-zulu
ENV grailsVersion 3.1.4
ENV gradleVersion 2.14

RUN echo "Hello World!"

RUN apt-get update && \
    apt-get install -y zip unzip curl

RUN curl -s "https://get.sdkman.io" | bash

RUN /bin/bash -c "source \"$HOME/.sdkman/bin/sdkman-init.sh\" && \
                  sdk install java ${javaVersion} && \
                  sdk install grails ${grailsVersion} && \
                  sdk install gradle ${gradleVersion}"

RUN mkdir /home/grails-app

WORKDIR /home/grails-app

ENTRYPOINT ["/bin/bash"]
