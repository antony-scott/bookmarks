# Setting up SQL Server in docker

Documentation on the mssql docker image can be found here - <https://hub.docker.com/_/microsoft-mssql-server>

```powershell
  docker volume create mssqlsystem
  docker volume create mssqluser
  docker pull mcr.microsoft.com/mssql/server
  docker container run -d -p 1433:1433 --volume mssqlsystem:/var/opt/mssql --volume mssqluser:/var/opt/sqlserver -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=password' --name sqlserver mcr.microsoft.com/mssql/server
```

If a new mssql server container is created using the previously created mssqlsystem docker volume then the SA password and EULA being accepted will be persisted and will **NOT** need to be specified when creating the new container.

## Next Steps
* create a docker volume pre-populated with databse backup files
* mount volume into correct path (so different pre-populated containers can be used)
* script the restore of the databases

# Further Reading
## Using volumes in docker

1. <https://dbafromthecold.com/2019/03/21/using-docker-named-volumes-to-persist-databases-in-sql-server/>
1. <https://docs.docker.com/storage/volumes/>
1. <https://blog.sqlauthority.com/2019/04/20/sql-server-docker-volume-and-persistent-storage/>
1. <http://www.centinosystems.com/blog/sql/persisting-sql-server-data-in-docker-containers-part-1/>
1. <https://sqlplayer.net/2019/12/using-sql-server-on-docker/>

## ASP.NET + MSSQL
* <https://docs.docker.com/compose/aspnet-mssql-compose/>

## Dockerize an ASP.NET Core application
* <https://docs.docker.com/engine/examples/dotnetcore/>
