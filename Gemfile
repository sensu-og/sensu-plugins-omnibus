source 'https://rubygems.org'

gem 'rake'

# Install omnibus
gem 'omnibus', :git => 'https://github.com/sensu/omnibus.git', :branch => 'sensu-testing'
#gem 'ffi', '1.9.18'
#gem 'ffi-yajl', '2.3.1'
gem 'ffi-yajl', :git => 'https://github.com/amdprophet/ffi-yajl.git', :branch => 'master'
gem 'artifactory', '2.5.1'
gem 'packagecloud-ruby', '1.0.5'

# This development group is installed by default when you run `bundle install`,
# but if you are using Omnibus in a CI-based infrastructure, you do not need
# the Test Kitchen-based build lab. You can skip these unnecessary dependencies
# by running `bundle install --without development` to speed up build times.
group :development do
  # Use Berkshelf for resolving cookbook dependencies
  gem 'berkshelf', '~> 5.6'

  # Use Test Kitchen for converging the build environment
  gem 'test-kitchen',            '~> 1.4'
  gem 'winrm'
  gem 'winrm-fs'
  gem 'winrm-elevated'
end

group :vagrant do
  gem 'kitchen-vagrant',         '~> 0.18'
end

group :ec2 do
  gem 'kitchen-ec2',             '~> 1.2'
end
