FROM golang:alpine

RUN apk update \
  && apk add git

COPY . /go/src/app

# Don't do this in production! Use vendoring instead.
#RUN go get -v app/server

RUN which sh bash

ENTRYPOINT ["/bin/sh"]


##RUN go env
#
#ENV GO111MODULE=on
#
##ENV GOPATH=/tmp
#
#RUN go env
#
#RUN go mod init app/server
#
##   RUN go mod vendor
#
#RUN go install app/server
#
#ENTRYPOINT ["/go/bin/server"]
#