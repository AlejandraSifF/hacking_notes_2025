#### Description

Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
```

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 54332 -U postgres pico`Password is `postgres
```
#### Consejos:
1. What does a SQL database contain?
   
![[Pasted image 20250415190135.png]]
![[Pasted image 20250415190204.png]]

#### Texto de terminal:
```
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte2-Web/8-SQL_Direct$ sudo apt install postgresql-client
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following additional packages will be installed:
  libpq5 postgresql-client-12
Suggested packages:
  postgresql-12 postgresql-doc-12
The following NEW packages will be installed:
  libpq5 postgresql-client postgresql-client-12
0 upgraded, 3 newly installed, 0 to remove and 0 not upgraded.
Need to get 1195 kB of archives.
After this operation, 4536 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 libpq5 amd64 12.22-0ubuntu0.20.04.2 [118 kB]
Get:2 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 postgresql-client-12 amd64 12.22-0ubuntu0.20.04.2 [1073 kB]
Get:3 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 postgresql-client all 12+214ubuntu0.1 [3940 B]
Fetched 1195 kB in 3s (413 kB/s)
Selecting previously unselected package libpq5:amd64.
(Reading database ... 82492 files and directories currently installed.)
Preparing to unpack .../libpq5_12.22-0ubuntu0.20.04.2_amd64.deb ...
Unpacking libpq5:amd64 (12.22-0ubuntu0.20.04.2) ...
Selecting previously unselected package postgresql-client-12.
Preparing to unpack .../postgresql-client-12_12.22-0ubuntu0.20.04.2_amd64.deb ...
Unpacking postgresql-client-12 (12.22-0ubuntu0.20.04.2) ...
Selecting previously unselected package postgresql-client.
Preparing to unpack .../postgresql-client_12+214ubuntu0.1_all.deb ...
Unpacking postgresql-client (12+214ubuntu0.1) ...
Setting up libpq5:amd64 (12.22-0ubuntu0.20.04.2) ...
Setting up postgresql-client-12 (12.22-0ubuntu0.20.04.2) ...
update-alternatives: using /usr/share/postgresql/12/man/man1/psql.1.gz to provide /usr/share/man/man1/psql.1.gz (psql.1.gz) in auto mode
Setting up postgresql-client (12+214ubuntu0.1) ...
Processing triggers for libc-bin (2.31-0ubuntu9.17) ...
yoli@Yoli:~/Fundamentos_Seguridad/Examen_1/Parte2-Web/8-SQL_Direct$ psql -h saturn.picoctf.net -p 54332 -U postgres pico
Password for user postgres:
psql (12.22 (Ubuntu 12.22-0ubuntu0.20.04.2), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 12, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# help
You are using psql, the command-line interface to PostgreSQL.
Type:  \copyright for distribution terms
       \h for help with SQL commands
       \? for help with psql commands
       \g or terminate with semicolon to execute query
       \q to quit
pico=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges
-----------+----------+----------+------------+------------+-----------------------
 pico      | postgres | UTF8     | en_US.utf8 | en_US.utf8 |
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 |
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(4 rows)

pico=# \c pico
could not translate host name "saturn.picoctf.net" to address: No address associated with hostname
Previous connection kept
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=#

```
## Solución
```
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
```
