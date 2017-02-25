FROM postgres:9.5.6

RUN apt-get update -qq && apt-get install -qqy postgresql-9.5-postgis-2.3 postgresql-9.5-postgis-2.3-scripts && rm -rf /var/lib/apt/lists/*

COPY docker-healthcheck /usr/local/bin/

HEALTHCHECK CMD ["docker-healthcheck"]

ENTRYPOINT ["docker-entrypoint.sh"]

EXPOSE 5432
CMD ["postgres"]
