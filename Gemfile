source 'http://rubygems.org'

used_installer = File.exist?("USED_INSTALLER")
USING_WINDOWS = !!((RUBY_PLATFORM =~ /(win|w)(32|64)$/) || (RUBY_PLATFORM=~ /mswin|mingw/))

# to avoid bundle install problems in Windows
if USING_WINDOWS
  gem 'eventmachine'#, '1.0.0.beta.4.1'
else
  gem 'spawn', '0.1.4'
end

gem 'rails', '3.0.19'
# NOTE: Shamisen version is defined in lib/version.rb
#

gem 'rake', '0.9.2.2'

# Bundle edge Rails instead:
# gem 'rails', :git => 'http://github.com/rails/rails.git'

gem 'app', '~> 1.0.3'
gem 'ffi', '1.1.1' #NOTE : was 1.1.0, updated to 1.1.1

platforms :jruby do
  gem 'jdbc-mysql', '5.1.13'
  gem 'jruby-openssl', '0.7.7'
  gem 'jruby-rack', '1.1.10'
  gem 'activerecord-jdbc-adapter', '1.2.2.1', :require => false
  gem 'rmagick4j', '0.3.7'
  gem 'warbler', '1.3.6'
  gem 'jruby-jars', '1.7.0'
end

platforms :ruby do
  gem 'thin', '1.4.1'
  gem 'mysql2', '< 0.3'
  # gem 'mysql2'  # will update with rails 3.1
end

gem 'redis-retry', :git => 'http://github.com/ramontayag/redis-retry' # NOTE: temporary requirement until this can be published as a gem
gem 'awetest-common', :git => 'https://github.com/3qilabs/awetest-common.git', :branch => 'release-2.0'
# :tag => 'v1.18.27'
gem 'resque', :git => 'http://github.com/radamanthus/resque.git', :tag => 'v1.19.7'

gem 'andand', '1.3.1'
gem 'sane', '0.23.5'
gem 'haml'
gem 'haml-rails'
gem 'authlogic', '3.1.0'
# gem 'annotate', '2.4.0'                           # generate/write the table schema in the model files
gem "declarative_authorization", '0.5.4'
gem 'ar_fixtures', '0.0.4'                        # so we can do rails g runner "Company.to_fixtures"
gem 'random_data', '1.5.2'                        # for generating random_data like faker
gem 'will_paginate', '3.0.2'
gem 'inherited_resources', '~> 1.3'             # provides common restful actions to our controllers so we don't need to repeat code
gem 'render_inheritable', '1.0.0'
#gem 'hpricot'                                    # this and ruby_parser only needed for inherited_views generator, uncomment if generating again.
gem 'ruby_parser', '2.3.1'
gem 'formtastic', '2.0.2'
gem 'rails3_acts_as_paranoid', '0.0.9'
gem 'wicked_pdf', '~> 0.9.0'

gem 'backbone-rails'

gem 'userstamp', '2.0.1'
gem 'rdoc', '3.11'


# gem 'delayed_job'
gem 'rufus-scheduler', '2.0.14'

gem 'selenium-client', '1.2.18'
gem 'selenium-selenese', '1.1.13'
gem 'mysql2', '< 0.3'

gem 'roo', '1.10.1'
gem 'spreadsheet', '0.6.9'
gem 'ekuseru', '0.3.10'
gem 'google-spreadsheet-ruby', '0.1.6'
gem 'rubyzip', '0.9.5'
gem 'nokogiri', '1.5.0'
gem 'minizip', '0.0.12'
gem 'draper', '~> 0.11.1'
gem 'parse-cron', '0.1.1', :require => 'cron_parser'
gem 'alm-rest-api'
gem 'nokogiri-happymapper', :require => 'happymapper'

# Rails Gem for providing inline Edit.
gem "best_in_place", "~> 0.2.0"

if USING_WINDOWS
  gem 'win32-open3'
  gem 'sys-uname', '0.8.5'
  # gem "vapir-ie"
  gem "watir", '1.8.1'
  # watirloo is not working - appears not to be used
  #gem "watirloo", :git => 'git@github.com:stalcottsmith/watirloo.git'
  gem "win32-process",'0.6.5'
end

# Support gems
gem "paperclip", '2.8.0'
gem "delayed_paperclip", '2.4.5.2'
gem "acts_as_versioned", '0.6.0'  # for versioning info on models

group :assets do
  gem 'compass', "0.11.5"
  gem 'compass-960-plugin', "0.10.4"
end

group :development do
  gem 'active_reload'
  gem 'require_relative'
  gem 'pry'
  # gem 'capistrano', '2.13.5'
  # gem 'rvm-capistrano'
  gem 'ruby-debug'
  # gem 'ruby-prof', '0.10.7' #NOTE: does not run on Jruby
end

gem 'faker', '1.0.1' # Put this here for now to stop warbler from complaining
group :test do
  gem 'steak'
  gem 'chronic'
  gem 'jasmine'
  # gem 'autotest-rails'
  gem 'capybara', '1.1.2'
  gem 'capybara-firebug'
  gem 'cucumber-rails'
  gem 'database_cleaner'
  gem 'email_spec'
  gem 'factory_girl_rails', '1.7.0'
  gem 'faker', '1.0.1'
  gem 'launchy'
  gem 'require_relative'
  gem 'rspec'
  gem 'rspec-rails'
  gem 'spork', '0.8.5'
  gem 'timecop', '0.3.5'
  gem 'ZenTest', '4.8.1'
end

# gem 'newrelic_rpm'
