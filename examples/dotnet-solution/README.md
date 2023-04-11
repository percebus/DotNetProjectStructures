## Remarks

- All projects (`.Tests` and otherwise) are created under a `dotnet/` folder.

## Folder Structure

```
│   .gitignore
│   My.Site.sln
│   stylecop.json
|
│   .dockerignore
│   docker-compose.yml
│   Dockerfile
|   ...
│
├───.github/
│   └───workflows/
|       └ ...
|
├───azure/
│   ├───pipelines/
|   |   └ ...
│   └───policies/
|       └ ...
|
├───dotnet/
│   ├───My.Site.AcceptanceTests/
│   ├───My.Site.ConsoleApp/
│   ├───My.Site.Domain.Lib/
│   ├───My.Site.Domain.Lib.Tests/
│   ├───My.Site.WebApp/
│   ├───My.Site.WebApp.Tests/
│   ├───Other.Thing.Foo.Lib/
│   └───Other.Thing.Foo.Lib.Tests/
|
├───node_modules/
|   └ ...
|
├───scripts/
│   └ ...
|
└───terraform/
        main.tf
        output.tf
        providers.tf
        values.tf
```

## Analysis

### Pros

- Like any other technology, things are grouped "by technology" (i.e. `dotnet/`)
- Groups `.Tests` projects & otherwise in a flattened fashion.

### Cons

None (I'm biased towards this setup)
