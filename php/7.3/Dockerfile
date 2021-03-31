FROM alpine:3.11


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
	php7-simplexml \
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
	php7-zip \
	php7-bz2 \
	php7-posix \
	php7-phar \
	php7-fileinfo \
	&& php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
	&& php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" \
	&& php composer-setup.php --install-dir=/bin --filename=composer \
	&& php -r "unlink('composer-setup.php');"
	&& rm -rf /var/cache/apk/*


ENTRYPOINT ["/usr/bin/php"]
CMD ["-v"]
