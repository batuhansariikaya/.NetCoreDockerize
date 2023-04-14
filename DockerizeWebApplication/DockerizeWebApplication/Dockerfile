FROM mcr.microsoft.com/dotnet/sdk:6.0
WORKDIR /project
COPY . .
RUN dotnet restore
RUN dotnet publish DockerizeWebApplication.csproj -c Release -o out
WORKDIR out
ENV ASPNETCORE_URLS="http://*:1453"
ENTRYPOINT ["dotnet", "DockerizeWebApplication.dll"]