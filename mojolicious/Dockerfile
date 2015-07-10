FROM perl
MAINTAINER Marco Musso <github@marcomusso.it>
RUN apt-get update && apt-get install gcc make wget curl apache2 gzip tar git
RUN cpanm -f -n Term::ReadLine::Perl Term::ReadKey Switch EV IO::Socket::Socks IO::Socket::SSL Net::DNS::Native Mojolicious
