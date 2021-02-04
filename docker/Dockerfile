LABEL org.opencontainers.image.source https://github.com/jmcarbo/redirecthttps
FROM golang:1.15 as golang
COPY . /redirecthttps
RUN cd /redirecthttps && go build -o redirecthttps .

FROM ubuntu:20.04
COPY --from=golang /redirecthttps/redirecthttps /redirecthttps
ENTRYPOINT "/redirecthttps"

