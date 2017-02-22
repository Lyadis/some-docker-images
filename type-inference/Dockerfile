FROM frekele/ant:1.9.7-jdk7u79


RUN apt-get -qq update && apt-get install --no-install-recommends -qqy \
	make \
	wget \
	unzip

RUN wget https://github.com/proganalysis/type-inference/archive/master.zip
RUN unzip master.zip
RUN mv type-inference-master /type-inference

WORKDIR /type-inference/inference-framework/jsr308-langtools/make
RUN ant
WORKDIR /type-inference/inference-framework/annotation-tools

ENV PATH=/opt/jdk1.7.0_79/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

RUN ant
WORKDIR /type-inference/inference-framework/checker-framework/checkers
RUN ant bindist
