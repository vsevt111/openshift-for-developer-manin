FROM quay.io/projectquay/golang:1.17
RUN go get -u github.com/go-sql-driver/mysql
ADD ./basic_reader.go ./
RUN go build -o basic_reader.go 
ENV PORT 8080
ENV MYSQL_USER TEST
ENV MYSQL_PASSWORD TEST
ENV MYSQL_DATABASE  mysql-vsevt111-dev.apps.sandbox-m2.ll9k.p1.openshiftapps.com
USER 1001
EXPOSE 8080
CMD ["./basic_reader"]

