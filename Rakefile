  namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola de Rake'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'invokes the environment task as a dependency'
  task :migrate => :environment do
    Student.create_table
  end

  task :environment do
  require_relative './config/environment'
end

  desc 'seeds the database with dummy data from a seed file'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
