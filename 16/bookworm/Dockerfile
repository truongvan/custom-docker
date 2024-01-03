FROM postgres:16

LABEL author="truongvan@live.com"

ENV POSTGIS_MAJOR 3
ENV POSTGIS_VERSION 3.2.1+dfsg-1.pgdg110+1

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
  "postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR=$POSTGIS_VERSION" \
  "postgresql-$PG_MAJOR-postgis-$POSTGIS_MAJOR-scripts=$POSTGIS_VERSION" \
  && rm -rf /var/lib/apt/lists/*
