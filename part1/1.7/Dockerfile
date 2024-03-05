FROM ubuntu:20.04
WORKDIR /usr/src/app
RUN apt-get update
RUN apt-get install -y curl
COPY exercise.sh .
RUN chmod +x exercise.sh
CMD ./exercise.sh