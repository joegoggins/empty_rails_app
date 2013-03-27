source 'https://rubygems.org'

gem 'rails', '3.2.3'
gem 'json'
gem 'cancan'
gem 'capistrano'

platform :ruby do
  gem 'therubyracer' #, '= 0.11.0beta5' # beta8 causes crazy compile errors on the mac
  group :libv8 do
    gem 'libv8', "~> 3.11.8"
  end
  gem 'ruby-oci8'
end

# Points to git master to grab this commit:
# https://github.com/rsim/oracle-enhanced/commit/35a244be11a4a9cb2e26418760cfc93bf47310bc
#
# When this commit is released in the gem, remove the :git business!
#
gem 'activerecord-oracle_enhanced-adapter', :git => 'https://github.com/rsim/oracle-enhanced.git'

gem 'execjs'

# Chosen-rails depends on this, DON't UPGRADE to 2.X unless you verify the other js libraries work
gem 'jquery-rails', '~> 1.0'
gem 'twitter-bootstrap-rails'
gem 'chosen-rails'
gem "select2-rails"
gem 'carrierwave'
gem 'sunspot_rails'
gem 'sunspot_solr'
gem 'composite_primary_keys', '5.0.8'
gem 'savon', '1.2.0'
gem 'spreadsheet'
gem 'state_machine'
gem 'less-rails'
gem 'exception_notification', :require => 'exception_notifier'
gem 'kaminari'

# IN HOUSE GEMS, (sub-module'd in)

# Gems used only for assets and not required
# in production environments by default.
group :assets do
  gem 'sass-rails',   '~> 3.2.3'
  gem 'coffee-rails', '~> 3.2.1'
  gem 'uglifier', '>= 1.0.3'
  gem 'compass-rails'
end

group :development do
  platform :ruby do
    # This ridiculousness is required to debug on ruby 1.9.3-p125
    # http://stackoverflow.com/questions/6438116/rails-with-ruby-debugger-throw-symbol-not-found-ruby-current-thread-loaderro
    # gem 'linecache19', '0.5.13' #, :path => "~/.rvm/gems/ruby-1.9.3-p#{RUBY_PATCHLEVEL}/gems/linecache19-0.5.13/"
    # gem 'ruby-debug-base19', '0.11.26' #, :path => "~/.rvm/gems/ruby-1.9.3-p#{RUBY_PATCHLEVEL}/gems/ruby-debug-base19-0.11.26/"
    # gem 'ruby-debug19', :require => 'ruby-debug'
    gem 'debugger'
    # gem 'brakeman'
    gem 'railroady'
    gem 'ruby-graphviz', :require => 'graphviz' # Used to graph state_machines
  end
  gem 'progress_bar'
end

group :test do
  platform :ruby do
    gem 'ruby-prof'
  end
  gem 'shoulda', '~> 3.0.1'
  gem 'mocha', :require => false
  gem 'capybara'
  gem 'capybara-webkit' # This can be a headache. Requires some crazy OS lib deps like Qt
  gem 'launchy'
  gem 'factory_girl_rails'
  gem 'cucumber-rails', :require => false
  gem 'database_cleaner'
end
