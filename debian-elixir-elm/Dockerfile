FROM ivandavid77/debian-elixir:latest

LABEL maintainer="Ivan D Barron <ivandavid77@gmail.com>"

ENV LANG en_US.UTF-8

# Prepare
RUN apt-get update && \
    apt-get -y install apt-utils && \
    apt-get -y install build-essential apt-transport-https && \
    apt-get -y install curl && \
    apt-get clean

# Node
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs

# Yarn
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get -y install yarn

# Elm
RUN yarn global add elm

# SASS
RUN apt-get update && \
    apt-get -y install ruby ruby-dev && \
    apt-get clean && \
    gem install sass

# ImageMagick
RUN apt-get update && \
    apt-get -y install imagemagick && \
    apt-get clean