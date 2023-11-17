# Copyright 2020 Amazon.com, Inc. or its affiliates. All Rights Reserved.
# SPDX-License-Identifier: Apache-2.0

FROM amazonlinux

RUN yum install unzip -y

RUN \
    cd tmp && \
    curl "https://awscli.amazonaws.com/awscli-exe-linux-$(arch).zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install

ENV HELLO="Hello from the enclave side!"
COPY hello.sh /bin/hello.sh

#CMD ["/bin/hello.sh"]
RUN aws s3 ls
