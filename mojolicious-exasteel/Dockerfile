FROM marcomusso/mojolicious:v1
MAINTAINER Marco Musso <github@marcomusso.it>

RUN cpanm -f -n MongoDB Compress::Zlib

RUN adduser --gecos "" --disabled-password --disabled-login mojouser

RUN git clone https://github.com/marcomusso/exasteel.git /home/mojouser/exasteel
RUN [ ! -d /home/mojouser/exasteel/log ] && mkdir /home/mojouser/exasteel/log

WORKDIR /home/mojouser
RUN chown -R mojouser:mojouser .

# WARNING: if the app uses some other services be sure they a reachable from this container
CMD morbo -v script/exasteel
EXPOSE 3001
