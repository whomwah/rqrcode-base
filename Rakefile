begin
  require "rake/testtask"
  require "standard/rake"

  Rake::TestTask.new(:test) do |t|
    t.libs << "test"
    t.libs << "lib"
    t.test_files = FileList["test/**/*_test.rb"]
  end

  task default: [:test, "standard:fix"]
rescue LoadError
  # no standard/rspec available
end
