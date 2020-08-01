#基于solr的7版
FROM solr:7.7.3

#维护人的信息
LABEL maintainer="Newmannhu <Newmannhu@qq.com>"


#创建名字为document的core
WORKDIR /opt/solr/server/solr
RUN mkdir document
WORKDIR /opt/solr/server/solr/document
RUN echo 'name=document' > core.properties
RUN mkdir data
RUN cp -r /opt/solr/server/solr/configsets/_default/conf ./conf

#复制smartcn的jar包
RUN cp /opt/solr/contrib/analysis-extras/lucene-libs/lucene-analyzers-smartcn-7.7.3.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/

