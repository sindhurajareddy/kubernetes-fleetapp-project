FROM arm64v8/amazoncorretto:17.0.5-al2022-RC-headless

LABEL maintainer="Richard Chesterwood <richard@inceptiontraining.co.uk>"

# Install necessary packages using yum package manager
RUN yum add --no-cache \
    wget \
    gzip \
    tar

# Download and extract Apache ActiveMQ
RUN wget -O activemq.tar.gz http://archive.apache.org/dist/activemq/5.17.3/apache-activemq-5.17.3-bin.tar.gz && \
    tar -xzf activemq.tar.gz && \
    rm activemq.tar.gz

ENV JAVA_HOME=/usr/bin/

CMD ["apache-activemq-5.17.3/bin/activemq", "console"]
