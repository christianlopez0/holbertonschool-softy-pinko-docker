FROM ubuntu:latest

RUN apt-get update && \
    apt-get upgrade -y

RUN echo 'echo "Hello, World!"' > /hello.sh && \
    chmod +x /hello.sh

CMD ["/hello.sh"]
