FROM esolang/build-base

RUN cd /tmp && \
    curl -m $TIMEOUT https://github.com/graue/esofiles/raw/master/adjust/impl/adjust.18.1.tar.gz -LO && \
    tar xzf adjust.18.1.tar.gz && \
    cd adjust.18.1 && \
    gcc -O2 -Wall -o adjust adjust.c && \
    mv adjust /usr/bin/adjust && \
    rm -rf /var/cache/apk/* /tmp/* && \
    ln -s /bin/script /bin/adjust

COPY script /root/script
