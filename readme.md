## Change Password
```
sudo docker exec -it sql1 /opt/mssql-tools/bin/sqlcmd \
-S localhost -U SA -P "<YourStrong@Passw0rd>" \
-Q 'ALTER LOGIN SA WITH PASSWORD="<YourNewStrong@Passw0rd>"'
```

## Connect to SERVER
```sudo docker exec -it sql1 "bash"```

Once inside the container, connect locally with sqlcmd. Sqlcmd is not in the path by default, so you have to specify the full path.

```/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "<YourNewStrong@Passw0rd>"```

## Create Table
```
CREATE DATABASE TestDB
SELECT Name from sys.Databases
GO
```

## EXIT
```QUIT```

