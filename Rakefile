namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end


  desc 'outputs hola to the terminal'
  task :hola do 
    puts "hola de Rake!"
  end
end 

namespace :db do 
  desc 'sets up the environment'
  task :environment do
    require_relative './config/environment.rb'
  end

  desc 'migrate stuff aka data to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the console'
  task :console do
    Pry.start
end