# based on https://github.com/MobileDevOps/flutter-sdk-image/blob/master/Dockerfile
FROM --platform=linux/amd64 ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive
ENV LANG en_US.UTF-8

# Add non-root user
RUN groupadd -r mobiledevops \
    && useradd --no-log-init -r -g mobiledevops mobiledevops

# Set non-root user as default
ENV HOME /home/mobiledevops
USER mobiledevops
WORKDIR $HOME/app

#ENV FLUTTER_VERSION="3.19.0"
#ENV FLUTTER_HOME "/home/mobiledevops/.flutter-sdk"
#ENV PATH $PATH:$FLUTTER_HOME/bin
#
## Download and extract Flutter SDK
#RUN mkdir $FLUTTER_HOME \
#    && cd $FLUTTER_HOME \
#    && curl --fail --remote-time --silent --location -O https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_${FLUTTER_VERSION}-stable.tar.xz \
#    && tar xf flutter_linux_${FLUTTER_VERSION}-stable.tar.xz --strip-components=1 \
#    && rm flutter_linux_${FLUTTER_VERSION}-stable.tar.xz
#
#RUN flutter precache