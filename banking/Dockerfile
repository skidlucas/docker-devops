FROM ubuntu:latest

RUN apt-get update && apt-get install -y mono-complete


COPY dotNet/server.exe /usr/banking/


EXPOSE 9090
CMD ["mono", "/usr/banking/server.exe"]
