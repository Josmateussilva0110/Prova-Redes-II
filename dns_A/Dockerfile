FROM ubuntu:latest

# Atualizar os repositórios e instalar o Bind9 e dnsutils
RUN apt-get update && apt-get install -y bind9 dnsutils

# Copiar os arquivos de configuração para os locais adequados
COPY named.conf.local /etc/bind/
COPY db.empresa-a /etc/bind/
COPY db.10.0.0 /etc/bind/  

# Definir permissões apropriadas
RUN chown root:bind /etc/bind/named.conf.local /etc/bind/db.empresa-a

# Expor as portas DNS
EXPOSE 53/udp 53/tcp

# Iniciar o serviço Bind9
CMD ["named", "-g"]
