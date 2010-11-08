desc 'Build Compass output'
task :compass => [:'compass:clean'] do
  system 'bundle exec compass compile -c config/compass.rb'
end

namespace :compass do
  desc 'Clean Compass output'
  task :clean do
    system 'rm -rf jekyll/stylesheets/*'
  end
  
  desc 'Start Compass watching the stylesheets directory'
  task :watch => [:'compass:clean'] do
    system 'bundle exec compass watch -c config/compass.rb'
  end
end

desc 'Start local server'
task :server do
  system 'bundle exec shotgun config.ru'
end