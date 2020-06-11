# Setting up SQL Server in docker

<https://hub.docker.com/_/microsoft-mssql-server>

```powershell
  docker pull mcr.microsoft.com/mssql/server
  docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=SomePassword!' -p 1433:1433 -d mcr.microsoft.com/mssql/server
```

# Further Reading
## Using volumes in docker

<https://docs.docker.com/storage/volumes/>
<https://blog.sqlauthority.com/2019/04/20/sql-server-docker-volume-and-persistent-storage/>
<https://dbafromthecold.com/2019/03/21/using-docker-named-volumes-to-persist-databases-in-sql-server/>
<http://www.centinosystems.com/blog/sql/persisting-sql-server-data-in-docker-containers-part-1/>
<https://sqlplayer.net/2019/12/using-sql-server-on-docker/>

## ASP.NET + MSSQL
<https://docs.docker.com/compose/aspnet-mssql-compose/>

## Dockerize an ASP.NET Core application
<https://docs.docker.com/engine/examples/dotnetcore/>
