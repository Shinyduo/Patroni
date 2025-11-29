FROM postgres:16

# Install Patroni and psycopg
RUN apt-get update && apt-get install -y --no-install-recommends \
      python3-pip python3-venv curl ca-certificates \
    && pip3 install --no-cache-dir "patroni[etcd]" \
    && rm -rf /var/lib/apt/lists/*

# Patroni will manage Postgres, data lives on a mounted volume
ENV PATRONI_POSTGRESQL_DATA_DIR=/var/lib/postgresql/data

# Expose Postgres and Patroni REST API
EXPOSE 5432 8008

CMD ["patroni"]
