FROM haproxy:2.9

COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

EXPOSE 5000

CMD ["haproxy", "-f", "/usr/local/etc/haproxy/haproxy.cfg"]
