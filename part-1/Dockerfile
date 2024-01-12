FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update && \
    apt-get -y install curl && \
    rm -rf /var/lib/apt/lists/*

COPY ./exercise-1-7.sh .

RUN chmod +x exercise-1-7.sh

CMD ["./exercise-1-7.sh"]
