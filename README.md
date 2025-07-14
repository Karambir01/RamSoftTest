# RamSoftTest
# steps to run
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.Tools

dotnet add package xunit
dotnet add package xunit.runner.visualstudio
dotnet add package Microsoft.NET.Test.Sdk
dotnet add package Microsoft.EntityFrameworkCore.InMemory

# Add initial migration
dotnet ef migrations add InitialCreate

# Apply migration to Azure SQL (edit your connection string first)
dotnet ef database update
# Need to replace the connection string in appsettings.json file.
