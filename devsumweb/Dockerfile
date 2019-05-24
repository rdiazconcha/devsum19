FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim AS base
WORKDIR /app
EXPOSE 80
EXPOSE 443

FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch AS build
WORKDIR /src
COPY ["devsumweb.csproj", ""]
RUN dotnet restore "devsumweb.csproj"
COPY . .
WORKDIR "/src/"
RUN dotnet build "devsumweb.csproj" -c Release -o /app

FROM build AS publish
RUN dotnet publish "devsumweb.csproj" -c Release -o /app

FROM base AS final
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "devsumweb.dll"]