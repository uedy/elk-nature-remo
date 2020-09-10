FROM fluent/fluentd:v1.11.2-debian-arm64-1.0

USER root
RUN apt-get update \

 && buildDeps=" \
      make gcc g++ libc-dev \
      wget bzip2 gnupg dirmngr \
    " \
 && apt-get install -y --no-install-recommends $buildDeps 
RUN gem install fluent-plugin-elasticsearch 
RUN gem sources --clear-all 
RUN rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/2.*/gems/fluentd-*/test

