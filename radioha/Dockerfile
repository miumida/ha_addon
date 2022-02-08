--FROM alpine:3.15
--RUN apk add --no-cache nodejs
--RUN apk add --no-cache npm
--RUN apk add --no-cache ffmpeg

RUN apt-get update
RUN apt-get install nodejs npm ffmpeg -y

WORKDIR /app
COPY index.js /app/
COPY package.json /app/
COPY radio-list.json /app/
COPY run.sh /app/
RUN chmod a+x /app/run.sh
RUN npm install
ENTRYPOINT [ "/app/run.sh" ]
