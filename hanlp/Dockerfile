#基于solr的7版
FROM solr:7.7.3

#维护人的信息
LABEL maintainer="Newmannhu <Newmannhu@qq.com>"

#创建名字为document的core
RUN /opt/solr/bin/solr create -c document
#将定制化的配置文件复制到document的conf下
ADD hanlp-managed-schema.xml /opt/solr/server/solr/document/conf/managed-schema

#复制hanlp-portable.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-1.7.8.jar /opt/solr/server/solr-webapp/webapp

#复制hanlp-lucene-plugin.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-lucene-plugin.jar /opt/solr/server/solr-webapp/webapp

#复制字库
ADD data /opt/solr/server/solr-webapp/webapp/data

