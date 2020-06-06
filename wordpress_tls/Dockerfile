FROM wordpress

RUN echo "export TERM=xterm LANG=en_US.UTF-8" >> ~/.bashrc \
    && apt-get update && apt-get -y install git \
    && rm -rf "/opt/letsencrypt" \
    && git clone https://github.com/letsencrypt/letsencrypt /opt/letsencrypt \
    && cd /opt/letsencrypt \
    && ./letsencrypt-auto --version
