namespace :greeting do 
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end 
  task :hola do 
    puts "hola de Rake!"
  end 
end


namespace :db do 
  desc 'migrate changes to your datbase'
  # task :environment do 
  #   require_relative './config/environment'
  # end
  task :migrate => :environment do
    Student.create_table
  end 
  desc 'seed the datbase with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end 

task :environment do 
  require_relative './config/environment'
end

desc 'drop into pry console'
task :console => :environment do
  pry.start
end