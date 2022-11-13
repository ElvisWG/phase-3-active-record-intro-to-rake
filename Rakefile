namespace :greeting do
  desc "Outputs hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "Outputs hola to the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "migrates changes to the database"
  task migrate: :environment do
    Student.create_table
  end
  desc "seed the database with some dummy data"
  task seed: :environment do
    require_relative "./db/seeds.rb"
  end

  task :environment do
    require_relative "./config/environment"
  end
end

desc "drop into the Pry console"
task console: :environment do
  Pry.start
end