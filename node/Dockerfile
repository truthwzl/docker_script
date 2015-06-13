FROM ubuntu
MAINTAINER Maxime Heckel
 
RUN apt-get update &&
apt-get install -y wget build-essential python python-dev python-pip python-virtualenv
RUN wget http://nodejs.org/dist/node-latest.tar.gz &&
tar xvzf node-latest.tar.gz &&
cd node-v* &&
./configure &&
CXX="g++ -Wno-unused-local-typedefs" make &&
CXX="g++ -Wno-unused-local-typedefs" make install &&
echo 'n# Node.jsnexport PATH="node_modules/.bin:$PATH"' >> /root/.bashrc
 
WORKDIR /data
