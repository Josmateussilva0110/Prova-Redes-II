FROM ubuntu:latest
RUN apt update && apt install -y iptables isc-dhcp-server
CMD ["sh", "-c", "service isc-dhcp-server start && sleep infinity"]
