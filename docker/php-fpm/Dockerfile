#
# PHP Setup
#

ARG PHP_VERSION=7.4.10

FROM php:${PHP_VERSION}-fpm-alpine

#
# Workspace User
#

ARG APP_USER_ID=1000
ARG APP_GROUP_ID=1000

RUN set -xe; \
    apk --update add \
        tzdata && \
        rm /var/cache/apk/*


#
# Set Timezone
#

ARG TIME_ZONE='Asia/Seoul'

RUN cp /usr/share/zoneinfo/${TIME_ZONE} /etc/localtime
