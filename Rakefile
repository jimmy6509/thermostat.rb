# encoding: US-ASCII
require 'rubygems'
gem 'hoe', '>= 2.1.0'
require 'hoe'
require 'fileutils'
require './lib/thermostat'

ENV['VERSION'] = Thermostat::VERSION

Hoe.plugin :newgem
Hoe.plugin :website
# Hoe.plugin :cucumberfeatures

# Generate all the Rake tasks
# Run 'rake -T' to see list of generated tasks (from gem root directory)
$hoe = Hoe.spec "thermostat" do
    self.developer 'Sean Dague', 'sean@dague.net'
    self.rubyforge_name = "sdaguegems"
    self.extra_rdoc_files = ["README.rdoc"]
    self.readme_file = "README.rdoc"
    self.extra_deps = [['temperature', '>= 1.0.0']]
    # self.extra_deps         = [['activesupport','>= 2.0.2']]
end

require 'newgem/tasks'
Dir['tasks/**/*.rake'].each { |t| load t }

# TODO - want other tests/tasks run by default? Add them to the list
# remove_task :default
# task :default => [:spec, :features]
