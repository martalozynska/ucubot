FROM microsoft/aspnetcore-build:2.0
ADD . /app
WORKDIR /app
RUN ["rm", "appsettings.Db.json"]
RUN ["mv", "appsettings.Db.docker.json", "appsettings.Db.json"]
RUN ["dotnet", "restore"]
RUN ["dotnet", "build"]

ENTRYPOINT ["dotnet", "run", "--server.urls", "http://*:80"]
