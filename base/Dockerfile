# Based on ubuntu Trusty Tahr LTS
FROM ubuntu:14.04.2

# install a basic setup for building code, with node as a high-powered scripting language
RUN apt-get -qqy update \
	&& apt-get -y install vim \
	&& apt-get -y install build-essential \
	&& apt-get install -y curl \
	&& apt-get -y install nodejs \
	&& update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10 \
	&& apt-get -y install npm \
	&& npm install -g nodemon

# users should probably override this in descendents
CMD ["/bin/bash"]

