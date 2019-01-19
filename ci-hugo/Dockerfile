#
# ci-hugo
#
# build:
#   docker build --force-rm -t posquit0/ci-hugo .
# run:
#   docker run \
#     --rm -it \
#     --network host \
#     --volume /var/run/docker.sock:/var/run/docker.sock \
#     --volume filebeat-data:/usr/share/filebeat/data \
#     --volume app-log:/log \
#     --name ci-hugo \
#     posquit0/ci-hugo
#

FROM alpine:3.7
LABEL maintainer="Byungjin Park <posquit0.bj@gmail.com>"
LABEL description="Test, build and deploy a Hugo static web in CI/CD pipelines"

# Install needed packages
RUN apk --no-cache add python py-pip ca-certificates curl git rsync

# Install Hugo
ENV HUGO_VERSION=0.38.2
ADD https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz /tmp/hugo.tar.gz
RUN tar xf /tmp/hugo.tar.gz hugo && \
  mv hugo /usr/bin/hugo && \
  rm /tmp/hugo.tar.gz

# Expose port
EXPOSE 1313
