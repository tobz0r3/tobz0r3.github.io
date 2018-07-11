FROM debian:jessie

RUN apt-get update
RUN apt-get install -y apache2 php5 vim wget
RUN a2enmod rewrite

# Apache configs
COPY web.conf /etc/apache2/sites-enabled/000-default.conf

# Import the DB
CMD /etc/init.d/apache2 start &&\
    bash