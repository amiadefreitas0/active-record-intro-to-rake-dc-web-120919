namespace :greeting do
  
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'hola should print out hola de Rake!'
    task :hola do
    puts 'hola de Rake!'
    end
end

desc 'console '
task :console do 
  binding.pry
end

namespace :db do
  # in order to create a db task it has to have access to 
  #  the enviornment. thats w
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate invokes the :environment task as a dependency'
  task :migrate => :environment do
    Student.create_table 
  end

  desc 'seeds the database with dummy data from a seed file'
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end

 



end
