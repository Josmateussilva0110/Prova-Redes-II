FROM ubuntu:latest
RUN apt update && apt install -y apache2 \
    && echo '<h1>Bem-vindo à Empresa B</h1>' > /var/www/html/index.html
CMD ["apache2ctl", "-D", "FOREGROUND"]
