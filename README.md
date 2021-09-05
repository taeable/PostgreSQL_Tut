# PostgreSQL_Tut
PostgreSQL Tutorial and projects

setup
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install postgresql

Or you can just run the setup script that does the above for you

./setup.sh


Check status

$sudo systemctl status postgresql



Config file locations

/etc/postgresql/11/main/postgresql.conf



Test if port is open

$ss -tunelp | grep 5432



Enter postgresql user

$sudo su - postgres



create a database user

$ createdb test_db -O test_user1



Add a test database user

$alter user test_user1 with password 'DBUserPassword



List users

$psql -l  | grep test_db



Enter console as that user

$psql test_db



Enter dummy data

%create table test_table ( id int,first_name text, last_name text );

%insert into test_table (id,first_name,last_name) values (1,'John','Doe'); 









