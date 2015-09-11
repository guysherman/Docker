FROM debian:testing

RUN echo "deb http://ftp.fr.debian.org/debian/ stretch main contrib non-free" >> /etc/apt/sources.list
RUN echo "deb-src http://ftp.fr.debian.org/debian/ stretch main contrib non-free" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y --no-install-recommends ca-certificates curl wget build-essential git libcppunit-1.13-0v5 libcppunit-dev
RUN apt-get build-dep ardour3 -y --no-install-recommends
RUN cd home && git clone git://git.ardour.org/ardour/ardour.git && cd ardour && ./waf configure --with-backends=dummy --test && ./waf build test
