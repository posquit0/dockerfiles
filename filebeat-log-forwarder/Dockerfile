#
# filebeat-log-forwarder
#
# build:
#   docker build --force-rm -t posquit0/filebeat-log-forwarder .
# run:
#   docker run \
#     --rm --it \
#     --network host \
#     --volume /var/run/docker.sock:/var/run/docker.sock \
#     --volume filebeat-data:/usr/share/filebeat/data \
#     --volume app-log:/log \
#     --name filebeat-log-forwarder \
#     posquit0/filebeat-log-forwarder
#

FROM docker.elastic.co/beats/filebeat:6.2.2
LABEL maintainer="Byungjin Park <posquit0.bj@gmail.com>"

# Copy configurations
COPY filebeat.yml /usr/share/filebeat/filebeat.yml
# Update file permission
USER root
