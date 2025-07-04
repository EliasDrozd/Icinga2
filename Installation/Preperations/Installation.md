# VM-Installation

## VM-Settings / Recommendations

For the Icinga2 Master-Node, a lightweight and easy to manage VM is the best recommendation. An example beeing a Ubuntu 24.02 LTS Server or similar.
The storage capacity should ideally be at least 40GB, unless you plan to store Icinga2 Graph and Check-Data for more than 1 year in total.

## Post-VM Installation

Always check that your VM is running on the latest Updates & all drivers are up to date:

`apt update && apt upgrade -y`

# Installing & Setting up DB (Database)

Icinga2 allows you to choose between your more favoured Database Variant, like MySQL, SQLLight oder MongoDB. I personally am more confident and more knowledged with MySQL but always choose the Database Type and Schema,
which is already familiar to you.
In our example, it is MySQL:

`apt install mysql-server`
`apt update`
`apt-upgrade`

## Configuring the Database

Now it is recommended to only give you permission to access the MySQL-Console and offcourse read, write and create Databases. This is done by adding a MySQL User with an according Password.
This is already enough for homelabs and home testing environments.

`sudo su <your masterpw>`
`sudo mysql -u root -p`

(-u is the user and -p is the password. For the innitial setup, do **not** adapt these, as MySQL will ask you to enter the required data with two seperate input fields)  
