FROM ubuntu:20.04
RUN apt update && apt install git -y && apt install maven -y && apt install default-jdk -y
WORKDIR /home/webapp/
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR /home/webapp/App42PaaS-Java-MySQL-Sample/
RUN echo "app42.paas.db.username = paasdb_user" > WebContent/Config.properties
RUN echo "app42.paas.db.port = 3306" >> WebContent/Config.properties
RUN echo "app42.paas.db.password = secret" >> WebContent/Config.properties
RUN echo "app42.paas.db.ip = database" >> WebContent/Config.properties
RUN echo "app42.paas.db.name = paasdb" >> WebContent/Config.properties
RUN mvn package