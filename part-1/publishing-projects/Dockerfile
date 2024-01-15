FROM ubuntu:18.04

WORKDIR /mydir

#Changed this ->  RUN curl -L https://github.com/ytdl-org/youtube-dl/releases/download/2021.12.17/youtube-dl -o /usr/local/bin/youtube-dl to the code below
RUN apt-get update && \
    apt-get install -y curl python && \
    curl -L https://github.com/ytdl-org/youtube-dl/releases/download/2021.12.17/youtube-dl -o /usr/local/bin/youtube-dl && \
    chmod a+x /usr/local/bin/youtube-dl


ENV LC_ALL=C.UTF-8

ENTRYPOINT ["/usr/local/bin/youtube-dl"]

# define a default argument
CMD ["https://imgur.com/gallery/xwJgflf"]

# volume command: $ docker run -v "$(pwd):/mydir" youtube-dl https://imgur.com/JY5tHqr

