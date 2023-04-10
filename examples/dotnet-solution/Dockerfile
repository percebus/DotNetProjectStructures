FROM mcr.microsoft.com/dotnet/sdk:7.0 AS base
WORKDIR /Project
COPY . .
RUN dotnet restore

FROM base AS test
RUN dotnet test -c Debug

FROM base AS bin
RUN dotnet publish -c Release -o bin

FROM mcr.microsoft.com/dotnet/aspnet:7.0
WORKDIR /app
COPY --from=bin /Project/bin .
ENTRYPOINT ["dotnet", "Acme.Banking.My.Site.WebApp.dll"]
