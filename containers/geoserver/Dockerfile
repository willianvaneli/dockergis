ARG GEOSERVER_VERSION=2.19.0
FROM kartoza/geoserver:$GEOSERVER_VERSION

USER root

RUN apt-get clean && apt-get update && apt-get install -y locales locales-all

# Define a linguagem padrão
ARG LOCALE=en_US.UTF-8
ENV LC_ALL $LOCALE
ENV LANG $LOCALE
ENV LANGUAGE $LOCALE

# Define a timezone
ARG TZ=UTC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Muda pra usuário não-root
USER 1000