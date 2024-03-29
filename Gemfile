source 'https://rubygems.org'

gem 'volt', '0.9.4'

# volt uses mongo as the default data store.
gem 'volt-mongo', '~> 0.1.0'
gem 'opal-jquery'

# The following gem's are optional for themeing
# Twitter bootstrap
gem 'volt-bootstrap', '~> 0.0.10'

# Simple theme for bootstrap, remove to theme yourself.
gem 'volt-bootstrap_jumbotron_theme', '~> 0.1.0'

# User templates for login, signup, and logout menu.
gem 'volt-user_templates', '~> 0.4.0'

# Add ability to send e-mail from apps.
gem 'volt-mailer', '~> 0.1.0'

# Use rbnacl for message bus encrpytion
# (optional, if you don't need encryption, disable in app.rb and remove)
#
# Message Bus encryption is not supported on Windows at the moment.
platform :ruby, :jruby do
  gem 'rbnacl', require: false
  gem 'rbnacl-libsodium', require: false
end

# Asset compilation gems, they will be required when needed.
gem 'csso-rails', '~> 0.3.4', require: false
gem 'uglifier', '>= 2.4.0', require: false

group :test do
  # Testing dependencies
  gem 'rspec', '~> 3.2.0'
  gem 'opal-rspec', '~> 0.4.2'
  gem 'capybara', '~> 2.4.2'
  gem 'selenium-webdriver', '~> 2.43.0'
  gem 'chromedriver2-helper', '~> 0.0.8'
  gem 'poltergeist', '~> 1.5.0'
end

# Server for MRI
platform :mri, :mingw do
  # The implementation of ReadWriteLock in Volt uses concurrent ruby and ext helps performance.
  gem 'concurrent-ruby-ext', '~> 0.8.0'

  # Thin is the default volt server, Puma is also supported
  gem 'thin', '~> 1.6.0'
  gem 'bson_ext', '~> 1.9.0'
end
