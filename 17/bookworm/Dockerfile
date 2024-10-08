FROM postgres:17

LABEL author="truongvan@live.com"

ENV POSTGIS_MAJOR 3

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
  "postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR" \
  "postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR-scripts" \
  && rm -rf /var/lib/apt/lists/*
