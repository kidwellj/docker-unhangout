FROM ubuntu:14.04
MAINTAINER Philippe Chiu

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y build-essential curl python git
RUN apt-get install -y nodejs npm nodejs-legacy
#RUN git clone https://github.com/joyent/node.git ; cd node ; git checkout v0.9.9 ; cd v0.9.9 ; ./configure ; make ; make install
#RUN rm -rf /tmp/node
RUN cd /opt ; git clone http://github.com/drewww/unhangout
RUN cd /opt/unhangout ; npm install
WORKDIR /opt/unhangout
CMD ["npm", "start"]