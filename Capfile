# Load DSL and set up stages
require "capistrano/setup"

# Include default deployment tasks
require "capistrano/deploy"

# Load the SCM plugin appropriate to your project:
#
# require "capistrano/scm/hg"
# install_plugin Capistrano::SCM::Hg
# or
# require "capistrano/scm/svn"
# install_plugin Capistrano::SCM::Svn
# or
require "capistrano/scm/git"
install_plugin Capistrano::SCM::Git

require 'capistrano/rails'
require "capistrano/bundler"
require "capistrano/rvm"
require 'capistrano/puma'my_app_name
install_plugin Capistrano::Puma, load_hooks: false
install_plugin Capistrano::Puma::Nginx
install_plugin Capistrano::Puma::Systemd


# Load custom tasks from `lib/capistrano/tasks` if you have any defined
Dir.glob("lib/capistrano/tasks/*.rake").each { |r| import r }
