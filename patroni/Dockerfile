FROM postgres:16

# Install Patroni and psycopg
RUN apt-get update && apt-get install -y --no-install-recommends \
      python3-pip python3-venv curl ca-certificates \
    && pip3 install --no-cache-dir "patroni[etcd]" "psycopg[binary]>=3.0.0" \
    && rm -rf /var/lib/apt/lists/*

ENV PATRONI_POSTGRESQL_DATA_DIR=/var/lib/postgresql/data

EXPOSE 5432 8008

CMD ["patroni"]
