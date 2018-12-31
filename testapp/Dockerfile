FROM ruby:2.6

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - && apt-get install -y nodejs

WORKDIR /usr/src/app

COPY Gemfile Gemfile.lock ./

RUN bundle install

COPY . .

CMD ["bundle", "exec", "puma", "-C", "config/puma.rb"]
