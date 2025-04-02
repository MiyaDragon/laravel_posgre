FROM alpine:3.6

RUN apk update && \
    apk add --no-cache nginx
RUN mkdir -p /run/nginx

RUN apk --no-cache add tzdata \
    && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && apk del tzdata

CMD nginx -g "daemon off;"
