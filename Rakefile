require 'pry'

task :environment do
  require_relative './config/environment'
end
#invokes the :environment task as a dependency

namespace :greeting do
  desc 'outputs hello to the terminal'
    task :hello do
      puts "hello from Rake!"
  end
  # greeting:hello should print out 'hello from Rake!'

  desc 'outputs hola to the terminal'
    task :hola do
      puts 'hola de Rake!'
  end
  # greeting:hola should print out 'hola de Rake!'
end



namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
      Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
      require_relative './db/seeds.rb'
  end
end
  #db:seed
  #seeds the database with dummy data from a seed file
  #create the students table in the database

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
