FROM docker.elastic.co/elasticsearch/elasticsearch:5.4.1

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-phonetic
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-icu

ENV "http.host=0.0.0.0" "script.inline=true" "script.stored=true" "xpack.security.enabled=false" "cluster.name=onlinetours"
