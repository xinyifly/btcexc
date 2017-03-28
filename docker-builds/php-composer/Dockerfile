FROM php
ADD https://mirrors.ustc.edu.cn/repogen/conf/debian-http-4-jessie \
  /etc/apt/sources.list
RUN apt-get update && apt-get -y dist-upgrade
RUN apt-get -y install git unzip
ADD https://getcomposer.org/installer /tmp/composer-setup.php
RUN php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer \
  && rm /tmp/composer-setup.php
RUN composer config -g repo.packagist composer https://packagist.phpcomposer.com
