FROM perl
MAINTAINER Marco Musso <github@marcomusso.it>
RUN apt-get update && apt-get install \
  curl \
  gcc \
  git \
  gzip \
  make \
  tar \
  wget
RUN cpanm -f -n \
  EV \
  IO::Socket::Socks \
  IO::Socket::SSL \
  Mojolicious
  Net::DNS::Native \
  Switch \
  Term::ReadLine::Perl \
  Term::ReadKey \
