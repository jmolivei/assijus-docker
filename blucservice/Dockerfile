FROM jetty:9.3.9-jre8
MAINTAINER crivano@jfrj.jus.br

#--- DOWNLOAD LATEST VERSION FROM GITHUB
RUN curl -s https://api.github.com/repos/assijus/blucservice/releases/latest \
  | grep browser_download_url \
  | grep blucservice.war \
  | cut -d '"' -f 4 \
  | wget -qi -

RUN pwd
RUN ls
#--- DEPLOY DO ARQUIVO .WAR ---
RUN mv blucservice.war /var/lib/jetty/webapps/ 

EXPOSE 8080
