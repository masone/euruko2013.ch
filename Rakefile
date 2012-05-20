task :default => 'build_and_deploy'

desc 'Deploys the build to gh-pages'
task :deploy do
  puts "Deploying ..."
  `cd build; git pull; echo 'euruko2013.ch' > CNAME; git add .; git commit -am 'build'; git push origin gh-pages`
end
task :d => :deploy

desc 'Builds the html'
task :build do
  puts "Building ..."
  `middleman build`
end
task :b => :build

desc 'Builds and deploys'
task :build_and_deploy => [:build, :deploy] do
end
task :bd => :build_and_deploy