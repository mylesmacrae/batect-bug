FROM mcr.microsoft.com/dotnet/sdk:3.1-alpine AS build
WORKDIR /src

COPY . .

WORKDIR /src/testproj
RUN dotnet publish testproj.csproj -c Release  -o /app

WORKDIR /app

ENTRYPOINT ["dotnet", "testproj.dll"]