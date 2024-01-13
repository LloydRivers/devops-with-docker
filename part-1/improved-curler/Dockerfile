FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update && \
    apt-get -y install curl && \
    rm -rf /var/lib/apt/lists/*

COPY ./script.sh .

RUN chmod +x script.sh

ENTRYPOINT ["./script.sh"]

CMD ["helsinki.fi"]
