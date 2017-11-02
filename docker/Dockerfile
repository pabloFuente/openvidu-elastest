FROM openvidu/openvidu-server-kms
MAINTAINER openvidu@gmail.com

RUN apt-get update && apt-get -y install sudo
RUN apt-get install -y curl

# Install Node
RUN sudo curl -sL https://deb.nodesource.com/setup_6.x | sudo bash - && sudo apt-get install -y nodejs

# Install http-server
RUN sudo npm install -g http-server

ADD openvidu-testapp/ /openvidu-testapp/
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 8443

CMD ["/usr/bin/supervisord"]
