### This docker file will create a custom drupal image with bootsrap theme 
# This docker image will be used from 


# Use the base image of drupal 8.6 
FROM drupal:8.6
# Run update and install git and cleanup the image 
RUN apt-get update \ 
    && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/*

#change the working dir
WORKDIR /var/www/html/themes
# Run Git clone
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap
#Change the work dir back to //var/www/html
WORKDIR /var/www/html



