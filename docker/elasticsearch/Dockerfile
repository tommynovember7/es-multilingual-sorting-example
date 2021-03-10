FROM elasticsearch:2.4

RUN bin/plugin install analysis-kuromoji && \
    bin/plugin install analysis-icu

ADD elasticsearch-concatenate-2.4.6.zip /tmp
RUN bin/plugin install file:///tmp/elasticsearch-concatenate-2.4.6.zip
