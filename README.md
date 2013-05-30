Windows-Gemfile
===============
Ruby on rails Installation on windows...

1. Download Ruby (1.8.7) and install it.
2. Download ruby-devKit, then follow the link :"https://github.com/oneclick/rubyinstaller/wiki/Development-Kit" step by step
3. Install bundler with "gem install bundler" command.
4. "bundle install" Thats all for ruby setup on windows. Following are some changes in Gemfile before bundle install in awetest setup. 

Follow the link for Mysql connectivity with our App: http://blog.mmediasys.com/2011/07/07/installing
-mysql-on-windows-7-x64-and-using-ruby-with-it/

Comment the line#10 in "config => initializers => redis-check.rb" (fail "ERROR: Redis database should be running. Run: redis-start"
  end)

Comment "capistrano" in gemfile

Replace :gem 'mysql2', '< 0.3'   
gem 'eventmachine', '1.0.0.beta.4.1' => gem 'eventmachine'    
gem "win32-process" =>  gem "win32-process",'0.5.5'   
"git@github.com:3qilabs/awetest-common.git" => "https://github.com/3qilabs/awetest-common.git"



For Awetest Following worker should be started: 1.bundle exec rake environment resque:work PID_FILE=/awetest/tmp/pids/resque_workers.pid QUEUE=regression_test_logs,notifications,documentation RAILS_ENV=development VVERBOSE=1 --trace


2. bundle exec resque-web -p 8282 -F
3. In shamisen=> shamisen.bat
4. redis-server
