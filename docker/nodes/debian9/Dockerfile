FROM debian:9
LABEL maintainer="javuto"

RUN apt update && apt install -y curl

RUN curl -# "https://osquery-packages.s3.amazonaws.com/deb/osquery_4.0.2_1.linux.amd64.deb" -o "/tmp/osquery.deb"
RUN dpkg -i "/tmp/osquery.deb"

COPY docker/nodes/debian9/wait.sh .

CMD [ "/bin/sh", "wait.sh" ]
