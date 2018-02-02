# begin with a ruby 2.2 base image
FROM ruby:2.2

# copy the provided drive binary so that it is available to us in the shell
# (specific version: drive v1.9.0)
COPY drive-190-bin /usr/local/bin/drive

# move inside /app (will be created if it doesn't already exist)
WORKDIR /app

# clone the two repositories which are necessary for our application
RUN ["git", "clone", "https://github.com/metakgp/mfqp-source.git", "mfqp-source"]
RUN ["git", "clone", "https://github.com/metakgp/mfqp.git", "mfqp"]

# move into the upload script directory and install all the required gems using
# bundler
WORKDIR /app/mfqp-source/scripts/upload

# create a test file (which will be used for uploading once and getting things
# done)
RUN echo "test" > test

ENV http_proxy 172.16.2.30:8080
ENV https_proxy 172.16.2.30:8080

RUN ["bundle", "install"]
