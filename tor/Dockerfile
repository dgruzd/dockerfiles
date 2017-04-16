FROM ubuntu:16.04

RUN echo "deb http://deb.torproject.org/torproject.org xenial main" >> /etc/apt/sources.list.d/tor.list && \
echo "deb-src http://deb.torproject.org/torproject.org xenial main" >> /etc/apt/sources.list.d/tor.list && \
gpg --keyserver keys.gnupg.net --recv A3C4F0F979CAA22CDBA8F512EE8CBC9E886DDD89 && \
gpg --export A3C4F0F979CAA22CDBA8F512EE8CBC9E886DDD89 | apt-key add && \
apt-get -qq update && \
apt-get install -y tor deb.torproject.org-keyring && \
echo "Log notice stdout" >> /etc/tor/torrc && \
echo "SocksPort 0.0.0.0:9050" >> /etc/tor/torrc && \
rm -rf /var/lib/apt/lists/*

# Default socks port
EXPOSE 9050

CMD [ "tor" ]
