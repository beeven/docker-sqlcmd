Docker sqlcmd image
=======

Supported tags and respective
------------

* latest [(13/Dockerfile)](https://github.com/beeven/docker-sqlcmd/blob/master/docker-entrypoint.sh)

### Usage:
Set up an alias to run it from docker image:
```bash
alias sqlcmd="docker run -it --rm beeven/docker-sqlcmd"
```
#### Known issue:
According to [this question](http://stackoverflow.com/questions/15103331/failure-to-connect-to-sql-server-from-linux), in order to connect to a named instance, you have to specify the port which the instance is using, e.p. ```sqlcmd -S 10.53.1.8,59013 -Uxxx -Pxxxx```.

### Documentation
[Connecting with sqlcmd (MSDN)](https://msdn.microsoft.com/en-us/library/hh568447.aspx)

[Connect to the Database Engine With sqlcmd (MSDN)](https://msdn.microsoft.com/en-us/library/ms188247.aspx)

### Example
```bash
$ sqlcmd -S 10.53.1.8 -U user_readonly

1> use TestDB;
2> go
```
