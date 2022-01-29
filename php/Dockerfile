FROM php:8.0-zts

RUN apt-get update -y && apt-get install -y git && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/man/?? /usr/share/man/??_* && \
    git clone https://github.com/krakjoe/parallel.git && \
    cd parallel && \
    phpize && \
    ./configure --enable-parallel && \
    make && \
    make install && \
    cd .. && \
    rm -rf parallel && \
    docker-php-ext-enable parallel
