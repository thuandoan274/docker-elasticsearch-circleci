FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4

ADD elasticsearch.yml /usr/share/elasticsearch/config/

USER root
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
RUN /usr/share/elasticsearch/bin/plugin install analysis-icu
COPY elasticsearch-analysis-vietnamese.zip / 
RUN /usr/share/elasticsearch/bin/plugin install file:///elasticsearch-analysis-vietnamese.zip
# elasticsearch cannot be executed by 'root' user for security reasons
# Details: https://discuss.elastic.co/t/why-is-it-elasticsearch-is-not-allowed-to-run-as-root/60413
USER elasticsearch

