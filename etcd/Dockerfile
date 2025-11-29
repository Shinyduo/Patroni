FROM quay.io/coreos/etcd:v3.5.15

# Railway will mount /var/lib/etcd via dashboard volume settings.
# DO NOT declare VOLUME here.

ENTRYPOINT ["/usr/local/bin/etcd"]
