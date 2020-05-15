FROM ruby:2.6.0
WORKDIR /mydir
COPY ./rails-example-project /mydir
RUN apt-get update && apt-get install -y nodejs
RUN bundle install
EXPOSE 3000
RUN rails db:migrate
CMD ["rails", "s"]
