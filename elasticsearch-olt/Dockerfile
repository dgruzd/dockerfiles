FROM docker.elastic.co/elasticsearch/elasticsearch:5.4.2

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-phonetic && \
/usr/share/elasticsearch/bin/elasticsearch-plugin install analysis-icu && \
/usr/share/elasticsearch/bin/elasticsearch-plugin remove x-pack

ENV http.host=0.0.0.0 script.inline=true script.stored=true cluster.name=onlinetours
