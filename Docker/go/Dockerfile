#Gerador do Binario GO
FROM golang:alpine3.18 AS compilador

WORKDIR /go/src/

COPY ola.go .

RUN /usr/local/go/bin/go build ola.go 

#Execucao do Binario
FROM scratch

WORKDIR /home
COPY --from=compilador /go/src/ola .

ENTRYPOINT [ "./ola" ]
