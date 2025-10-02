# Dockerfile
FROM ruby:3.1

# Install build tools
RUN apt-get update -qq && apt-get install -y build-essential nodejs

# Create app directory
WORKDIR /usr/src/app

# Install bundler
RUN gem install bundler jekyll

# Copy site files
COPY . .

# Install gems
RUN bundle install

# Expose Jekyll default port
EXPOSE 4000

# Default command: build & serve
CMD ["bundle", "exec", "jekyll", "serve", "--host", "0.0.0.0", "--livereload", "--force_polling"]
