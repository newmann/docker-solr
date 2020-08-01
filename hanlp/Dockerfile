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

#复制hanlp-portable.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-1.7.8.jar /opt/solr/server/solr-webapp/webapp

#复制hanlp-lucene-plugin.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-lucene-plugin-1.1.6.jar /opt/solr/server/solr-webapp/webapp

#复制字库
#ADD data /opt/solr/server/solr-webapp/webapp/data

