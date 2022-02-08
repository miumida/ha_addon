FROM ubuntu:20.04

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install nodejs npm ffmpeg -y

WORKDIR /app
COPY index.js /app/
COPY package.json /app/
COPY radio-list.json /app/
COPY run.sh /app/
RUN chmod a+x /app/run.sh
RUN npm install
ENTRYPOINT [ "/app/run.sh" ]
