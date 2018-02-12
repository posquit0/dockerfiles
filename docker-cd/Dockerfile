#
# docker-cd
#
# build:
#   docker build --force-rm -t posquit0/docker-cd .
# run:
#   docker run --rm --name docker-cd posquit0/docker-cd
#

FROM docker:18.01.0-ce
LABEL maintainer "Byungjin Park <posquit0.bj@gmail.com>"

# Install needed packages
RUN apk --no-cache add python py-pip git openssh-client

RUN pip install awscli
