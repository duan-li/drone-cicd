FROM alpine:3.9

RUN apk add --update php7 \
	php7-fpm \
	php7-bcmath \
	php7-ctype \
	php7-json \
	php7-mbstring \
	php7-openssl \
	php7-tokenizer \
	php7-xmlrpc \
	php7-xmlreader \
	php7-xml \
	php7-xmlwriter \
	php7-pdo_mysql \
	php7-pdo_sqlite \
	php7-pdo_pgsql \
	php7-pdo_dblib \
	php7-pdo_odbc \
	php7-pdo \
	php7-pecl-xdebug \
	php7-pecl-imagick \
	php7-pecl-yaml \
	php7-pecl-redis \
	php7-pecl-memcached \
	php7-soap \
	php7-curl \
	php7-ldap \
	php7-session \
	php7-gd \
	php7-opcache \
	php7-common \
	composer \
	&& rm -rf /var/cache/apk/*


ENTRYPOINT ["/usr/bin/php"]
CMD ["-v"]
