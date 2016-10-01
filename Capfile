# Load DSL and Setup Up Stages
require 'capistrano/setup'
require 'capistrano/deploy'

require 'capistrano/rails'
require 'capistrano/bundler'
require 'capistrano/puma'

# some requires above

task :use_rvm do
  require 'capistrano/rvm'
end

task :use_rbenv do
  require 'capistrano/rbenv'
end

#task production: :use_rvm
task production: :use_rbenv
task staging: :use_rbenv

set :rbenv_custom_path, '/home/bbsoft0/.rbenv/versions/2.3.1/bin'
set :rbenv_ruby, '2.3.1'

# Loads custom tasks from `lib/capistrano/tasks' if you have any defined.
Dir.glob('lib/capistrano/tasks/*.rake').each { |r| import r }