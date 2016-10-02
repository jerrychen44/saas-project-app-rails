# README

This is a Project Management Service app.
(under developing.)



Note: Before you new a rails app.....
1.I use PostgreSQL in this project.
 Need to download locally. ref: http://postgresapp.com/
 Set the $PATH. ref: http://postgresapp.com/documentation/cli-tools.html
2.rails new saas-project-app -d postgresql
3.Create role in postgresql

$ createuser -P -d -e saas-rails
Enter password for new role:
Enter it again:
CREATE ROLE "saas-rails" PASSWORD 'md5bacfb395f4bc66f925e38be00f64a52f' NOSUPERUSER CREATEDB NOCREATEROLE INHERIT LOGIN;

4.modify your /config/database.yml (development and test)
development:
  <<: *default
  database: saas-project-app_development
  username: saas-rails
  password: password



5.rails db:migrate and rake db:setup, your db/schema.rb should add on line enable_extension "plpgsql".
6.you can start the server by rails s, and check the localhost:3000
7.if page shows the welcome , then postgreSQL setting done. You can see them in GUI tool Postico.
