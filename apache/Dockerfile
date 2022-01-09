FROM httpd:latest

RUN apt-get update -y \
    && apt-get install vim -y \
    && rm -rf /var/lib/apt/lists/*

ADD ./index.html /home/sites/default/index.html
ADD ./test.php /home/sites/default/test.php

ADD ./httpd.conf /usr/local/apache2/conf/httpd.conf

EXPOSE 80 443

CMD [ "httpd-foreground"]
