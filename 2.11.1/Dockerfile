FROM eclipse-temurin:17-jre

ARG PUSLAR_VERSION=2.11.1

RUN mkdir /pulsar && chmod g+w /pulsar

RUN wget "https://archive.apache.org/dist/pulsar/pulsar-${PUSLAR_VERSION}/apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz" -O apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz \
    && wget "https://archive.apache.org/dist/pulsar/pulsar-${PUSLAR_VERSION}/apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz.sha512" -O apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz.sha512  \
    && cat apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz.sha512 |sha512sum -c - \
    && tar -zxvf apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz \
    && mv apache-pulsar-${PUSLAR_VERSION}/* /pulsar/ \
    && rm -rf apache-pulsar-${PUSLAR_VERSION} apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz apache-pulsar-${PUSLAR_VERSION}-bin.tar.gz.sha512

WORKDIR /pulsar

ENV PULSAR_ROOT_LOGGER=INFO,CONSOLE

EXPOSE 6650 8080

CMD [ "bin/pulsar", "standalone"]
