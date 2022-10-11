namespace :greeting do
  desc "Outputs Hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to the terminal"
  task :hola do 
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative "./config/environment"
end

namespace :db do
  desc "seed the database with dummy data"
  task seed: :environment do
    require_relative "./db/seeds"
  end

  desc "migrate changes to our database"
  task migrate: :environment do
    Student.create_table
  end
end

desc "drop into the Pry console"
task console: :environment do
  Pry.start
end