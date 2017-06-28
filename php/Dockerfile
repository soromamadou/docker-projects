FROM php:7-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
        libsqlite3-dev \
        libssl-dev \
        libcurl3-dev \
        libxml2-dev \
        libzzip-dev \
        apt-utils \
        zlib1g-dev \
        libicu-dev \
        g++ \
    && docker-php-ext-install -j$(nproc) bcmath calendar ctype curl dba dom exif fileinfo ftp gettext hash iconv json mbstring mcrypt mysqli opcache pdo pdo_mysql pdo_sqlite phar session simplexml soap sockets tokenizer xml xmlwriter zip \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd

CMD ["php-fpm"]
#bcmath calendar ctype curl dba dom exif fileinfo ftp gettext hash iconv json mbstring mcrypt mysqli opcache pdo pdo_mysql pdo_sqlite phar session simplexml soap sockets tokenizer xml 


## && docker-php-ext-install -j$(nproc) bcmath calendar ctype curl dba dom exif fileinfo ftp gettext gmp hash iconv imap interbase intl json ldap mbstring mcrypt mysqli oci8 odbc opcache pcntl pdo pdo_dblib pdo_firebird pdo_mysql pdo_oci pdo_odbc pdo_pgsql pdo_sqlite pgsql phar posix pspell readline recode reflection session shmop simplexml snmp soap sockets spl standard sysvmsg sysvsem sysvshm tidy tokenizer wddx xml xmlreader xmlrpc xmlwriter xsl zip \
   
##bcmath bz2 calendar ctype curl dba dom enchant exif fileinfo filter ftp gd gettext gmp hash iconv imap interbase intl json ldap mbstring mcrypt mysqli oci8 odbc opcache pcntl pdo pdo_dblib pdo_firebird pdo_mysql pdo_oci pdo_odbc pdo_pgsql pdo_sqlite pgsql phar posix pspell readline recode reflection session shmop simplexml snmp soap sockets spl standard sysvmsg sysvsem sysvshm tidy tokenizer wddx xml xmlreader xmlrpc xmlwriter xsl zip