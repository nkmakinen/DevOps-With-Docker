FROM ruby:2.6.0

WORKDIR /rails
RUN apt-get update && apt-get install -y wget curl apt-utils git software-properties-common
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/docker-hy/rails-example-project.git /rails
RUN gem install bundler
RUN bundle install
RUN rails db:migrate RAILS_ENV=development
EXPOSE 3000

CMD ["rails", "s"]