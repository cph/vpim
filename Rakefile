require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "vpim"
    gem.summary = %Q{vCard and iCalendar support}
    gem.description = %Q{vCard and iCalendar support, the standard for exchange and storage of contact information and calendars}
    gem.email = "sam@github"
    gem.homepage = "http://github.com/sam-github/vpim"
    gem.authors = ["Sam Roberts"]
    gem.add_dependency "plist"
    gem.add_development_dependency "jeweler"
    gem.add_development_dependency "turn"
    #gem.add_development_dependency "shoulda", ">= 0"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

begin
  require 'rcov/rcovtask'
  Rcov::RcovTask.new do |test|
    test.libs << 'test'
    test.pattern = 'test/**/test_*.rb'
    test.verbose = true
  end
rescue LoadError
  task :rcov do
    abort "RCov is not available. In order to run rcov, you must: sudo gem install spicycode-rcov"
  end
end

task :default => :test
