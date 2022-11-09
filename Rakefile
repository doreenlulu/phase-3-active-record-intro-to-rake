# task :hello do
#   puts "hello from Rake!"
# end

namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end


task :environment do
  require_relative './config/environment'
end


namespace :db do
  task migrate: :environment do
    Student.create_table
  end

  task seed: :environment do
    require_relative './db/seeds'
  end
end


task console: :environment do
  Pry.start
end