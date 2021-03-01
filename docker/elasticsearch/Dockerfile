FROM docker.elastic.co/elasticsearch/elasticsearch:7.11.1

RUN elasticsearch-plugin install analysis-kuromoji && \
    elasticsearch-plugin install analysis-icu

ADD elasticsearch-concatenation-token-filter-6.5.0.1.zip /tmp
RUN elasticsearch-plugin install file:///tmp/elasticsearch-concatenation-token-filter-6.5.0.1.zip
