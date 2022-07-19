FROM phpmyadmin:latest

RUN apt-get -y update && \
    apt-get upgrade -y && \
    apt-get -y --no-install-recommends install curl unzip

RUN curl https://files.phpmyadmin.net/themes/darkwolf/5.1/darkwolf-5.1.zip -o /var/www/html/themes/darkwolf.zip \
&& unzip /var/www/html/themes/darkwolf.zip -d /var/www/html/themes/ \
&& rm -rfv /var/www/html/themes/darkwolf.zip

RUN apt-get remove curl unzip -y && apt-get autoremove