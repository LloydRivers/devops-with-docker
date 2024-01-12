FROM devopsdockeruh/simple-web-service:alpine

CMD server

# docker build -t web-server .
# docker run -p 8080:8080 web-server

# output: [GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
# - using env:   export GIN_MODE=release
# - using code:  gin.SetMode(gin.ReleaseMode)

#[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
#[GIN-debug] Listening and serving HTTP on :8080
#[GIN] 2024/01/12 - 15:48:59 | 200 |       3.943ms |   192.#168.215.1 | GET      "/"
#[GIN] 2024/01/12 - 15:49:00 | 200 |         168µs |   192.168.215.1 | GET      "/favicon.ico"


