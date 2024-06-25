FROM php:8.0-apache

# Install necessary extensions
RUN docker-php-ext-install mysqli

# Enable mod_rewrite for Apache
RUN a2enmod rewrite

# Set work directory
WORKDIR /var/www/html

# Copy the application files
COPY src/ /var/www/html/

# Expose port
EXPOSE 80



