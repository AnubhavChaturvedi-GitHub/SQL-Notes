# SQL-Notes
visit website to download the setup of sql :- [Download](https://dev.mysql.com/downloads/installer/)

1. To display the databases abliable in PC
```shell
show database;
```
Output :
```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.01 sec)

mysql>
```
2. To select the databases from the list EG: Mysql
```shell
use mysql;
```
3. show all the table from the databases
```shell
show tables;
```
output 
```
+------------------------------------------------------+
| Tables_in_mysql                                      |
+------------------------------------------------------+
| columns_priv                                         |
| component                                            |
| db                                                   |
| default_roles                                        |
| engine_cost                                          |
| func                                                 |
| general_log                                          |
| global_grants                                        |
| gtid_executed                                        |
| help_category                                        |
| help_keyword                                         |
| help_relation                                        |
| help_topic                                           |
| innodb_index_stats                                   |
| innodb_table_stats                                   |
| ndb_binlog_index                                     |
| password_history                                     |
| plugin                                               |
| procs_priv                                           |
| proxies_priv                                         |
| replication_asynchronous_connection_failover         |
| replication_asynchronous_connection_failover_managed |
| replication_group_configuration_version              |
| replication_group_member_actions                     |
| role_edges                                           |
| server_cost                                          |
| servers                                              |
| slave_master_info                                    |
| slave_relay_log_info                                 |
| slave_worker_info                                    |
| slow_log                                             |
| tables_priv                                          |
| time_zone                                            |
| time_zone_leap_second                                |
| time_zone_name                                       |
| time_zone_transition                                 |
| time_zone_transition_type                            |
| user                                                 |
+------------------------------------------------------+
38 rows in set (0.01 sec)
```
4. Create Table in my sql
```shell
CREATE TABLE STUDENTS(SN INT(2),NAME VARCHAR(10),DOB VARCHAR(10));
```
output
```
Query OK, 0 rows affected, 1 warning (0.02 sec)

```
5. Insert the value in Table
```shell
INSERT INTO STUDENTS VALUES(01,'ANUBHAV','08/10/2003');
```
output
```
Query OK, 1 row affected (0.01 sec)
```
6. Display the table
```shell
SELECT *FROM STUDENTS;
```
output
```
+------+---------+------------+
| SN   | NAME    | DOB        |
+------+---------+------------+
|    1 | ANUBHAV | 08/10/2003 |
+------+---------+------------+
1 row in set (0.00 sec)
```
