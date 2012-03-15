# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "movr_acts_as_likeable"
  gem.homepage = "http://github.com/darmou/movr_acts_as_likeable"
  gem.license = "MIT"
  gem.summary = %Q{Social Media Acts As Likeable}
  gem.description = %Q{This gem is heavily influenced by acts_as_voteable & acts_as_rateable, can be used for Thumbs Up/Down or Likes/Dislikes situations, also helps to get the Percentage of Likes to Dislikes and vice versa on an Object, to depict average popularity.}
  gem.email = "dmoulder@qtome.com"
  gem.authors = ["Daryl Moulder, https://github.com/umerfarooq"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

require 'rcov/rcovtask'
Rcov::RcovTask.new do |test|
  test.libs << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
  test.rcov_opts << '--exclude "gems/*"'
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "movr_acts_as_likeable #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
