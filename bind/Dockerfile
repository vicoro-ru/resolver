FROM alpine:edge
MAINTAINER "Mikhail Ivanov <alisterosenheim@gmail.com>"
RUN apk add --no-cache bind
#COPY --chown=named:named dconf /etc/bind
#COPY --chown=named:named keys /var/cache/bind
EXPOSE 53/udp
EXPOSE 53/tcp
EXPOSE 953/tcp
ENTRYPOINT ["/usr/sbin/named"]
CMD ["-g", "-c", "/etc/bind/named.conf.recursive", "-u", "named"]