## ERROR 1045 (28000): Access denied for user 'chenss'@'localhost' (using password: NO)
### Environment:
ubuntu 16.04
### Solution:
Find the configuration file with **mysqld** field in the mysql directory,add the "skip-grant-tables" under the **mysqld** filed.
(the configuration file is like **my.cnf** or **mysqld.cnf**)
