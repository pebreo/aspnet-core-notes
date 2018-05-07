

### Installation
Download the ASP.NET Core for Mac
Then:
```bash
ln -s /usr/local/share/dotnet/dotnet /usr/local/bin/
```

### Hello World
```
dotnet new razor -o myapp
cd myapp
dotnet run
```

### Hello World MVC
```
dotnet new mvc
dotnet run
```

### Docker

##### Dockerfile
```
FROM microsoft/dotnet:latest

COPY . /app

WORKDIR /app

RUN ["dotnet","restore"]
RUN ["dotnet","run"]

EXPOSE 5000/tcp
ENTRYPOINT ["dotnet","run","--server.urls","http://0.0.0.0:5000"]
```


## Sources

https://www.youtube.com/watch?v=_hy7lD9Mngw&feature=youtu.be