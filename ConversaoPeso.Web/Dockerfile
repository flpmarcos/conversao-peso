FROM mcr.microsoft.com/dotnet/sdk:5.0 as builder
WORKDIR /app
COPY . .
RUN dotnet publish -c Release

FROM mcr.microsoft.com/dotnet/aspnet:5.0
WORKDIR /app
COPY --from=builder /app/bin/Release/net5.0/publish .
CMD ["dotnet", "ConversaoPeso.Web.dll"]