FROM php:8.0-apache

# Install necessary extensions
RUN docker-php-ext-install mysqli

# Enable mod_rewrite for Apache
RUN a2enmod rewrite

# Set work directory
WORKDIR /var/www/html

# Copy the application files
COPY src/ /var/www/html/

# Change owner of /var/www to www-data and set permissions
RUN chown -R www-data:www-data /var/www && chmod -R 755 /var/www

# Debugging step to check permissions and user
RUN ls -ld /var/www /var/www/html && ls -l /var/www/html
RUN whoami

# Expose port
EXPOSE 80


