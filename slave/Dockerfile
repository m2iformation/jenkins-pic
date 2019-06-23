FROM alpine:3.6
LABEL maintainer "Adrian B. Danieli - https://github.com/sickp"

COPY rootfs /

RUN apk add --no-cache openssh \
  && sed -i s/#PermitRootLogin.*/PermitRootLogin\ yes/ /etc/ssh/sshd_config \
  && echo "root:root" | chpasswd

EXPOSE 22
ENTRYPOINT ["/entrypoint.sh"]
