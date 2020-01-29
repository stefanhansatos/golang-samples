FROM golang:alpine

RUN apk update \
  && apk add git

COPY . /go/src/app

ENV GO111MODULE=on

RUN pwd

#RUN go mod init app/server

#RUN go mod vendor

#RUN go install /go/src/app/server


# Don't do this in production! Use vendoring instead.
RUN go get -v app/server

RUN go install app/server

ENTRYPOINT ["/go/bin/server"]


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