FROM openvidu/openvidu-server-kms
MAINTAINER openvidu@gmail.com

ADD openvidu-testapp/ /openvidu-testapp/
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 8443

CMD ["/usr/bin/supervisord"]
