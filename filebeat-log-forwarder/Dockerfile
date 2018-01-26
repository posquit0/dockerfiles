#
# filebeat-log-forwarder
#

FROM docker.elastic.co/beats/filebeat:6.1.2
LABEL maintainer "Byungjin Park <posquit0.bj@gmail.com>"

# Copy configurations
COPY filebeat.yml /usr/share/filebeat/filebeat.yml
# Update file permission
USER root
RUN chown filebeat /usr/share/filebeat/filebeat.yml
USER filebeat
