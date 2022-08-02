FROM wordpress:6
COPY ./custom.ini $PHP_INI_DIR/conf.d/

WORKDIR /var/www/html

# ENTRYPOINT resets CMD
ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["apache2-foreground"]