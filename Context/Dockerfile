FROM ubuntu:focal

LABEL maintainer "VCityTeam"
LABEL source.repo "https://github.com/VCityTeam/UD-Demo-vcity-geovolume-docker.git"

RUN apt-get update

# The container will serve (through http) the client code 

######### Install the UD-Viz demo per se (client code) and build it
# Node version 14 is required. For its installation (on focal) refer to e.g.
#  https://computingforgeeks.com/install-node-js-14-on-ubuntu-debian-linux/
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get install -y nodejs
RUN node --version
RUN npm --version
RUN apt-get install -y git
RUN git --version

######### Install GeoVolume-Server

WORKDIR /
RUN git clone https://github.com/VCityTeam/GeoVolume-Server.git
WORKDIR /GeoVolume-Server
RUN npm install


EXPOSE 3000
CMD [ "npm", "start"]
