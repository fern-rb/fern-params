require 'bundler/gem_tasks'
require 'rake/testtask'
require 'fern/params/version'

Rake::TestTask.new(:test) do |t|
  t.libs << 'test'
  t.libs << 'lib'
  t.test_files = FileList['test/**/*_test.rb']
end

task release: :build do
  `gem push pkg/fern-params-#{Fern::Params::VERSION}.gem`
end

task default: :test
