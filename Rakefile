require "bundler/gem_tasks"
require "rspec/core/rake_task"

RSpec::Core::RakeTask.new(:spec)

task :default => :spec

namespace :assets do
  desc 'Update Office UI Fabric assets'
  task update: :clean do
    sh 'npm install'
    sh 'cp -r node_modules/office-ui-fabric-js/dist/components/**/*.scss vendor/assets/scss/components'
    sh 'cp -r node_modules/office-ui-fabric-js/dist/css/fabric.components* vendor/assets/css'
    sh 'cp -r node_modules/office-ui-fabric-js/dist/js/*.js vendor/assets/js'

    puts "Updated to the latest version of Office UI Fabric"
  end

  desc 'Remove old office-ui-fabric assets'
  task :clean do
    sh 'rm -rf vendor'
    sh 'mkdir -p vendor/assets/js/ vendor/assets/scss/ vendor/assets/css vendor/assets/scss/components'
    sh 'echo \'@import "components/*"\' > vendor/assets/scss/fabric.components.scss'
  end
end
