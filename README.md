# sidekiq-test
implement sidekiq 


##1. Install Ruby

  Check installation 

  ruby -v 

##2. Install Rails 
   sudo gem install rails --no-ri --no-rdoc

   Check installation    
   rails -v 

##3. Create a new ruby project 
  rails new sidekiq-test

##4. Add packages in Gemfile 
  
    cd sidekiq-test
    vi GemFile 
     - add following lines 
      gem 'httparty'
      - MongoDB Wrapper
      gem 'mongoid', '~> 5.0'
      gem 'bson', '~> 3.0'
      - Email Server
      - gem 'aws-ses'
      - AWS SDK
      gem 'aws-sdk', '~> 2'
      - Sinatra
      gem 'sinatra'
      - Sidekiq 
      gem 'sidekiq'
      - Sidekiq Failures
      gem 'sidekiq-failures'
      gem 'ruby-push-notifications'


##5. Install packages 
    
    bundle install 

##6. Start Rails server 

    #rails s

##7. Install redis 
      brew install redis  

##8. Start redis server 
    redis-server


##9 start sidekiq 
    bundle exec sidekiq -C config/sidekiq.yml
