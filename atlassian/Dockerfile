FROM cptactionhank/atlassian-confluence:latest

LABEL maintainer="crazyrico@qq.com"

USER root

# 将代理破解包加入容器
COPY ./atlassian/atlassian-agent.jar /opt/atlassian/confluence/
# COPY ./db/init.sql /docker-entrypoint-initdb.d/1-init.sql

# 设置启动加载代理包
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/confluence/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/confluence/bin/setenv.sh


# java -jar atlassian-agent.jar -d -m crazyrico@qq.com -n crazyrico -p conf -o http://172.16.10.50 -s BTW4-2T4Y-9BTK-R0DP
