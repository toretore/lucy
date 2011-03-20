require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the lucy plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.libs << 'test'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the lucy plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Lucy'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification. See http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "lucy"
  gem.homepage = "http://github.com/toretore/lucy"
  gem.license = "MIT"
  gem.summary = %Q{Rails plugin for generating javascript files from Ruby objects}
  gem.description = gem.summary
  gem.email = ""
  gem.authors = ["Tore Darell"]
  gem.add_development_dependency 'activesupport'
end
Jeweler::RubygemsDotOrgTasks.new
