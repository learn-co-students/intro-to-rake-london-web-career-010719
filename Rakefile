namespace :greeting do
  desc 'puts hello to the terminal '
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'puts hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end


task :environment do
  require_relative './config/environment'
end

# the reason for having a Rake console is to input pry statements and to debug etc...
desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end


# migrating means
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
