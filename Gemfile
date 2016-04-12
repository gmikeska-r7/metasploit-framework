source 'https://rubygems.org'
# Add default group gems to `metasploit-framework.gemspec`:
#   spec.add_runtime_dependency '<name>', [<version requirements>]
gemspec name: 'metasploit-framework'

# rails-upgrade staging gems
gem 'metasploit-yard',        github: 'rapid7/metasploit-yard',        branch: 'staging/rails-upgrade'
gem 'metasploit-erd',         github: 'rapid7/metasploit-erd',         branch: 'staging/rails-upgrade'
gem 'yard-metasploit-erd',    github: 'rapid7/yard-metasploit-erd',    branch: 'staging/rails-upgrade'
gem 'metasploit-concern',     github: 'rapid7/metasploit-concern',     branch: 'staging/rails-upgrade'
gem 'metasploit-model',       github: 'rapid7/metasploit-model',       branch: 'staging/rails-upgrade'
gem 'metasploit_data_models', github: 'rapid7/metasploit_data_models', branch: 'staging/rails-upgrade'
gem 'metasploit-credential',  github: 'rapid7/metasploit-credential',  branch: 'bug/MS-906/remove-manual-removeal-of-order-statement'

# separate from test as simplecov is not run on travis-ci
group :coverage do
  # code coverage for tests
  # any version newer than 0.5.4 gives an Encoding error when trying to read the source files.
  # see: https://github.com/colszowka/simplecov/issues/127 (hopefully fixed in 0.8.0)
  gem 'simplecov'
end

group :development do
  # Markdown formatting for yard
  gem 'redcarpet'
  # generating documentation
  gem 'yard'
  # for development and testing purposes
  gem 'pry'
  # module documentation
  gem 'octokit', '~> 4.0'
  # rails-upgrade staging gems
end

group :development, :test do
  # automatically include factories from spec/factories
  gem 'factory_girl_rails'
  # Make rspec output shorter and more useful
  gem 'fivemat'
  # running documentation generation tasks and rspec tasks
  gem 'rake'
  # Define `rake spec`.  Must be in development AND test so that its available by default as a rake test when the
  # environment is development
  gem 'rspec-rails'
end

group :test do
  # cucumber extension for testing command line applications, like msfconsole
  gem 'aruba'
  # cucumber + automatic database cleaning with database_cleaner
  gem 'cucumber-rails', :require => false
  gem 'shoulda-matchers'
  # Manipulate Time.now in specs
  gem 'timecop'
end
