# Web Development
Making a personal log about steps to setup, develop and deploy web apps with backend code and databases.

## Databases

### MySQL
Create development user and databaser for testing:
```
> create database db_name_dev;
> GRANT ALL PRIVILEGES ON db_name_dev.* TO 'dev_user'@'%' IDENTIFIED BY 'dev_password';
```
If there is initial data from any database, it can be passed with:
```
$ mysqldump --user=[dev_user] --host=[host or ip] -P [port] -p [source_db_name] > ~/backup_filename.sql
```
To transfer data to new database use:
```
$ mysql -h [host or ip] -P [port] -u [user with needed privilegies] -p
> source [local path to file.sql]
```
