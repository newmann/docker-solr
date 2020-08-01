#基于solr的7版
FROM solr:7

#维护人的信息
LABEL maintainer="Newmannhu <Newmannhu@qq.com>"

#创建名字为document的core
RUN create_core -c document

#复制hanlp-portable.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-1.7.8.jar /opt/solr/server/solr-webapp/webapp

#复制hanlp-lucene-plugin.jar至镜像/opt/solr/server/solr-webapp/webapp下
ADD hanlp-lucene-plugin.jar /opt/solr/server/solr-webapp/webapp

#复制字库
ADD data /opt/solr/server/solr-webapp/webapp/data

EXPOSE 8983