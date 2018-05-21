

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


### Controller

```csharp
using Microsoft.AspNetCore.Mvc;
using System.Text.Encodings.Web;

namespace MvcMovie.Controllers
{
    public class HelloWorldController : Controller
    {
        // 
        // GET: /HelloWorld/

        public string Index()
        {
            return "This is my default action...";
        }

        // 
        // GET: /HelloWorld/Welcome/ 

        public string Welcome()
        {
            return "This is the Welcome action method...";
        }
    }
}

```

### Custom route params
```csharp
# in startup.cs
app.UseMvc(routes =>
{
    routes.MapRoute(
        name: "default",
        template: "{controller=Home}/{action=Index}/{id?}");
});

# in the controller
public string Welcome(string name, int ID = 1)
{
    return HtmlEncoder.Default.Encode($"Hello {name}, ID: {ID}");
}
```


Resources

https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app-xplat/adding-controller?view=aspnetcore-2.0

simple api crud
https://medium.com/@pielegacy/an-in-depth-guide-into-a-ridiculously-simple-api-using-net-core-8f5edd427b0