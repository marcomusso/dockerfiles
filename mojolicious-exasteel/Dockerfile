FROM marcomusso/mojolicious:v1
MAINTAINER Marco Musso <github@marcomusso.it>

RUN cpanm -f -n MongoDB Compress::Zlib

RUN adduser --gecos "" --disabled-password --disabled-login mojouser

RUN git clone https://github.com/marcomusso/exasteel.git /home/mojouser/exasteel
RUN [ ! -d /home/mojouser/exasteel/log ] && mkdir /home/mojouser/exasteel/log

WORKDIR /home/mojouser
RUN chown -R mojouser:mojouser .

# install an editor, just in case
RUN apt-get install -y vim

# WARNING: if the app uses some other services be sure they a reachable from this container

# DEVELOPMENT
CMD cd exasteel && morbo -v script/exasteel

# PRODUCTION
#CMD cd exasteel && hypnotoad script/exasteel

EXPOSE 3000 3001
