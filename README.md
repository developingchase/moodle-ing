# moodle-ing
Scripts for working with moodle

When upgrading from 2.9.1 to 3.0, I had to do the following:
Created a back up VM
Put site in maintenance mode
Copied over the entire directory to a back up folder
Downloaded the latest 3.0 TGZ from Sourceforge
Unzipped it
My DB was already InnoDB compliant
I had to upgrade some of the tables from Antelope to Barracude
php admin/cli/mysql_compressed_rows.php --list
php admin/cli/mysql_compressed_rows.php --showsql
copied and pasted the output SQL statements then logged into the MYSQL database and manually executed them
I had to chown all of the moodle files to www-data.www-data
I also had to copy over some of the plugins I was using previously
I used the built in plugin check to validate which ones I need to move


I need to make sure the cron job still works!
