# mysql-5.6

# Steps to install Mysql 5.6

    • Download mysql 5.6 for ubuntu.
        ◦ Download “mysql-5.6.42-linux-glibc2.12-x86_64.tar.gz”  file to download folder 
        ◦ Open terminal  (Ctr + Alt + T) and do follow the steps below.
- cd Downloads 
- sudo rm /var/lib/mysql/ -R
- sudo rm /etc/mysql/ -R
- sudo apt-get autoremove mysql* --purge
- sudo apt-get remove apparmor
- sudo groupadd mysql
- sudo useradd -g mysql mysql
- sudo tar xvzf mysql-5.6.42-linux-glibc2.12-x86_64.tar.gz 
- sudo mv mysql-5.6.42-linux-glibc2.12-x86_64 /usr/local/mysql
- cd /usr/local/mysql
- sudo chown -R mysql:mysql *
- sudo apt-get install libaio1
- sudo scripts/mysql_install_db --user=mysql
- sudo chown -R root .
- sudo chown -R mysql data
- sudo cp support-files/my-default.cnf /etc/my.cnf
- sudo bin/mysqld_safe --user=mysql &
- sudo cp support-files/mysql.server /etc/init.d/mysql.server
- sudo bin/mysqladmin -u root password '123456'
- sudo ln -s /usr/local/mysql/bin/mysql /usr/local/bin/mysql
- sudo reboot


# Command lines for mysql server
Start mysql server
- sudo /etc/init.d/mysql.server start
Stop mysql server
- sudo /etc/init.d/mysql.server stop
Check status of mysql
- sudo /etc/init.d/mysql.server status
Enable mysql on startup
- sudo update-rc.d -f mysql.server defaults
Disable mysql on startup (Optional)
- sudo update-rc.d -f mysql.server remove

#Steps to install Mysql client
- sudo apt install mysql-client-core-5.7
- sudo mysql -u root -p
    • Enter your password was set above.
    • Enter “SELECT VERSION();” to terminal to check mysql server version.

# Steps to install MySQL Workbench
    • Click Ubuntu software icon on taskbar.
    • Search and select to “MySQL Workbench” then install by click “install” button.
    • After the software was installed click on “launch” button to run the app.

https://www.processio.com/install-mysql-5-5-5-6-ubuntu-16-04-xenial/ => This link also helps to install Mysql on Ubuntu.
