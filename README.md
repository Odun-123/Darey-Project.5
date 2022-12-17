# Darey-Project.5
# CLIENT-SERVER ARCHITECTURE WITH MYSQL
Step 1. Creating an 2 AWS instance & Connecting to it using Windows Terminal

I named  the first one db server and the second one client

![Pro5- aws instance ](https://user-images.githubusercontent.com/117018714/208266457-e35cf96b-37e3-46de-ae45-30003a20d255.png)

Step 2 : Installing MySQL Server and MySQL Client on each of the instances respectively

First thing we will do is to install mysql server in the mysql instance.

To do that, we simply run the code below: 'sudo apt install mysql-server.

Next, we install mysql client on the mysql client instance. To do that, we simply run the code below: 'sudo apt install mysql-client'

Step 3: Configuring MySQL server to allow connections from remote hosts.

In order to configure mysql server instance to allow coonnections from remote host, I ran the code below: 'sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf'

While inside this file, I replaced the bind address from the default '127.0.0.1' to '0.0.0.

![Pro5-bind address](https://user-images.githubusercontent.com/117018714/208266772-29b042c2-05ae-49f0-a37f-bf6a712df0d3.png)

Step 4: Configuring the security group of mysql server instance to allow the ip address of mysql client with port 3300

Next step was I had to configure the security group of mysql server instance to allow the ip address of mysql client instance.

Step 6: Connecting to mysql server from mysql client

Once the user had been created, next was to connect to the myql server instance from the mysql client instance. To do that, I simply ran the code below: 'mysql -u remote_user -h 172.31.83.161 -p'

After that, i ran the code below: 'show databases;

![pro5-database result](https://user-images.githubusercontent.com/117018714/208268001-dfe7d926-9fec-4e5a-a757-0baa683cde60.png)
