## ERROR 1045 (28000): Access denied for user 'chenss'@'localhost' (using password: NO)
### Environment:
ubuntu 16.04
### Solution:
Find the configuration file with **mysqld** field in the mysql directory,add the "skip-grant-tables" under the **mysqld** filed.
(the configuration file is like **my.cnf** or **mysqld.cnf**)

## ERROR 1055 :this is incompatible with sql_mode=only_full_group_by
### Environment:
ubuntu 16.04
### Solution:
Enter sql,type `SET sql_mode=" ";`to change sql_mode set.
