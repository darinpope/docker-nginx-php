FROM nginx:1.15.5-alpine

ENV TZ=America/New_York

RUN apk add tzdata \
    && cp /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone

CMD ["nginx"]

EXPOSE 80 443