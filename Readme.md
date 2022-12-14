-   Tutorials
    -   [dotnet](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/?WT.mc_id=dotnet-35129-website)
    -   [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
-   Check version
    -   `dotnet --list-sdks`
-   Create an api
    -   `dotnet new webapi -f net6.0`
        -   [Program.cs](./Program.cs) is the entry point
        -   [Controllers/](./Controllers/WeatherForecastController.cs) has all the controllers mapped to respective apis
        -   [ContosoPizza.cproj](./ContosoPizza.csproj) holds the meta data
        -   [Properties/launchSettings.json](./Properties/launchSettings.json) Defines where and how project is hosted
-   Build
    -   `dotnet run` (to view, visit https://localhost:{PORT}/weatherforecast)
        -   Locates the project file at the current directory.
        -   Retrieves and installs any required project dependencies for this project.
        -   Compiles the project code.
        -   Hosts the web API with the ASP.NET Core Kestrel web server at both an HTTP and HTTPS endpoint.
    -   `dotnet dev-certs https --trust`
        -   Enforces to trust the installed certificate
-   Test
    -   `dotnet tool install -g Microsoft.dotnet-httprepl`
        -   http repl (read evaluate print loop)
        -   _-g_ for global installation
        -   installs the .NET HTTP REPL command-line tool
        -   check the following for details on how to use **httprepl** tool
            -   [Test the web API - from point 3](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/3-exercise-create-web-api)
            -   [Passing parameter to get req - from point 7](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/6-exercise-add-controller)
            -   [crud requests - from point 6](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/8-exercise-implement-crud)
-   [Understanding controllers](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/4-aspnet-controllers)
-   Creating api for pizzas
    -   Create [pizza model](./Models/Pizza.cs)
    -   Create [pizza service](./Services/PizzaService.cs)
    -   Create [pizza controller](./Controllers/PizzaController.cs)
    -   `dotnet build` : Builds the project
    -   Get by id api in [pizza controller](./Controllers/PizzaController.cs)
    -   [Understanding CRUD actions in ASP.NET Core](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/7-crud)
    -   Add CRUD apis to [pizza controller](./Controllers/PizzaController.cs)
- [summary and more tutorials](https://learn.microsoft.com/en-in/training/modules/build-web-api-aspnet-core/9-summary)