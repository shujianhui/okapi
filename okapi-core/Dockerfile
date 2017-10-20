FROM folioci/openjdk8-jre-alpine:latest

ENV VERTICLE_FILE okapi-core-fat.jar
ENV PORT 9130
LABEL org.folio.healthcheck.cmd="curl --fail http://localhost:${PORT}/_/proxy/health || exit 1"

# Copy your fat jar to the container
COPY target/${VERTICLE_FILE} /usr/verticles/${VERTICLE_FILE}

# Okapi runs on this port by default
EXPOSE $PORT

HEALTHCHECK CMD curl --fail http://localhost:${PORT}/_/proxy/health || exit 1

