Repositório somente para estudos!

## Tutorial: criar uma API Web com ASP.NET Core

Path:
`/ Docs / .NET / ASP.NET Core / Aplicativos API Web / Tutoriais / Criar uma API Web`

Links:
* https://docs.microsoft.com/pt-br/aspnet/core/tutorials/first-web-api
* https://www.youtube.com/watch?v=TTkhEyGBfAk

## Adicionar um contexto de banco de dados

https://docs.microsoft.com/pt-br/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio-code#create-a-web-project

**Versão atual**

```bah
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory
```

**Versão 3.1.4**

```bah
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 3.1.4
dotnet add package Microsoft.EntityFrameworkCore.InMemory --version 3.1.4
```

---

## Scaffold de um controlador

https://docs.microsoft.com/pt-br/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio-code#scaffold-a-controller

**Comandos:**

```bash
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet tool install -g dotnet-aspnet-codegenerator
dotnet tool update -g dotnet-aspnet-codegenerator
dotnet aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers
```

**Comandos para versão 3.\*:**

```bash
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 3.*
dotnet add package Microsoft.EntityFrameworkCore.Design --version 3.*
dotnet tool install --global dotnet-aspnet-codegenerator --version 3.*
dotnet tool update -g Dotnet-aspnet-codegenerator --version 3.*
```

_Output:_

```xml
  <ItemGroup>
    <PackageReference Include="Microsoft.EntityFrameworkCore.Design" Version="3.*">
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
      <PrivateAssets>all</PrivateAssets>
    </PackageReference>
    <PackageReference Include="Microsoft.EntityFrameworkCore.InMemory" Version="3.*" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="3.*" />
    <PackageReference Include="Microsoft.VisualStudio.Web.CodeGeneration.Design" Version="3.*" />
</ItemGroup>
```

**Comandos para versão 3.1.4:**

```bash
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 3.1.4
dotnet add package Microsoft.EntityFrameworkCore.Design --version 3.1.4
dotnet tool install --global dotnet-aspnet-codegenerator --version 3.1.4
dotnet tool update -g Dotnet-aspnet-codegenerator --version 3.1.4
dotnet aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers
```

_Output:_

```xml
  <ItemGroup>
    <PackageReference Include="Microsoft.EntityFrameworkCore.Design" Version="3.1.4">
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
      <PrivateAssets>all</PrivateAssets>
    </PackageReference>
    <PackageReference Include="Microsoft.EntityFrameworkCore.InMemory" Version="3.1.4" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="3.1.4" />
    <PackageReference Include="Microsoft.VisualStudio.Web.CodeGeneration.Design" Version="3.1.4" />
  </ItemGroup>
```

**Comando para gerar o Controller `TodoItemsController`:**

```bash
dotnet aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers
```
