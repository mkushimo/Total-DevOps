## Use below for to choose the Postgre SQL version for Linux - RHEL.
```
https://www.postgresql.org/download/linux/redhat/
```

## Install the repository RPM:
```
dnf install -y https://download.postgresql.org/pub/repos/yum/reporpms/EL-8-x86_64/pgdg-redhat-repo-latest.noarch.rpm
```

## Disable the built-in PostgreSQL module:
```
dnf -qy module disable postgresql
```

## Install PostgreSQL:
```
dnf install -y postgresql11-server
```

## Initialize the database and enable automatic start:
```
/usr/pgsql-11/bin/postgresql-11-setup initdb
systemctl enable postgresql-11
systemctl start postgresql-11
systemctl status postgresql-11 
```

## Switch to to postgres user
```
sudo su - postgres
```

## Start PostgreSQL CLI.
```
psql
```

## Set the password for postgres user as follows.
```
\password postgres
```

## Create a user in PostgreSQL
```
create user mithuntechnologies with encrypted password 'passw0rd';
```

## Create a database in PostgreSQL
```
create database employees;
```

## Grant all privileges to the user mithuntechnologies to employees database.
```
grant all privileges on database employees to mithuntechnologies;
```

## To Quit the PostgreSQL Client type as follows
```
 \q
```

## Search the pg_hba.conf in Linux server as follows.
```
find / -name pg_hba.conf  
```

## Need enable pg_hba.conf file to access the Postgre SQL server from out side (Remote Connections).  
```
vi /var/lib/pgsql/11/data/pg_hba.conf 
```

## IPv4 local connections:
```
host    all             all             127.0.0.1/32        ident
Replace Ip address and authentication method as follows.
```

## IPv4 local connections:
```
host    all             all             0.0.0.0/0            md5
find / -name postgresql.conf
vi /var/lib/pgsql/11/data/postgresql.conf 
```

## - Connection Settings -
```
#listen_addresses = 'localhost'

listen_addresses = '*'
```

## Important Points 
Default Port number for Postgre SQL server is 5432

## Create a table called EMPLOYEE.
```
CREATE TABLE EMPLOYEES (
	ID INT PRIMARY KEY NOT NULL,
	NAME TEXT NOT NULL,
	DESIGNATION TEXT NOT NULL,
	SALARY REAL NOT NULL,
	JOIN_DATE DATE
);

INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (1, 'Radha Reddy L', 'Director', '100000.00', '2019-08-01');
INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (2, 'Supriya Reddy L', 'Director', '100000.00', '2019-08-01');
INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (3, 'Ruthvik Reddy L', 'CTO', '50000.00', '2019-08-01');
INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (4, 'Mithun Reddy L', 'CA', '50000.00', '2019-08-01');
INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (5, 'Shishir Reddy L', 'Software Engineer', '40000.00', '2019-08-01');
INSERT INTO EMPLOYEES (ID, NAME, DESIGNATION,SALARY,JOIN_DATE) VALUES (6, 'Manan Reddy L', 'DevOps Engineer', '40000.00', '2019-08-01');
 
COMMIT; 
To see the EMPLOYEES table data use below SQL Query
SELECT * FROM EMPLOYEES;
``` 
 
 
 
