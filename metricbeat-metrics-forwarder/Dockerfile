#
# metricbeat-metrics-forwarder
#
# build:
#   docker build --force-rm -t posquit0/metricbeat-metrics-forwarder .
# run:
#   docker run \
#     --rm --it \
#     --network host \
#     --volume=/proc:/hostfs/proc:ro \
#     --volume=/sys/fs/cgroup:/hostfs/sys/fs/cgroup:ro \
#     --volume=/:/hostfs:ro \
#     --volume /var/run/docker.sock:/var/run/docker.sock \
#     --volume metricbeat-data:/usr/share/metricbeat/data \
#     --name metricbeat-metrics-forwarder \
#     posquit0/metricbeat-metrics-forwarder -system.hostfs=/hostfs
#

FROM docker.elastic.co/beats/metricbeat:6.2.2
LABEL maintainer="Byungjin Park <posquit0.bj@gmail.com>"

# Copy configurations
COPY metricbeat.yml /usr/share/metricbeat/metricbeat.yml
# Update file permission
USER root
