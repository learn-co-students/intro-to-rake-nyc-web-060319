
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'set up environ'
task :environment do
  require_relative './config/environment.rb'
end


desc 'console start'
task :console => :environment do
  puts "Imagine this is a console"
  Pry.start
end

namespace :db do
  desc 'migrates db'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end