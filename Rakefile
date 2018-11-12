
namespace :greeting do

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'ouput hola'
  task :hola do
    puts "hola de Rake!"
  end

end




namespace :db do

  task :environment do
  require_relative './config/environment'
  end

  desc 'migrate changes to db'
  task :migrate => :environment do
    Student.create_table

  end

  desc 'seed db with dummy data'
  task :seed do
require_relative './db/seeds.rb'
  end
end
