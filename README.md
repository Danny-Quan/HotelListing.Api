# HotelListing.Api

HotelListing.Api is a simple RESTful Web API for managing hotels and countries built with ASP.NET Core targeting .NET 10. It uses Entity Framework Core with SQL Server and exposes OpenAPI/Swagger documentation.

## Features
- CRUD endpoints for hotels (and countries)
- EF Core Code-First migrations
- OpenAPI (Swagger) documentation

## Prerequisites
- .NET 10 SDK
- SQL Server (local or remote)
- PowerShell (recommended) or any terminal

## Getting started
1. Clone the repo:

   git clone https://github.com/Danny-Quan/HotelListing.Api.git
   cd HotelListing.Api

2. Restore and build:

   dotnet restore
   dotnet build

3. Configure the database connection

   Update the ConnectionStrings section in appsettings.json (or use user secrets / environment variables) to point to your SQL Server instance. For example:

   {
	 "ConnectionStrings": {
	   "HotelListingDb": "Server=localhost;Database=HotelListingDb;Trusted_Connection=True;MultipleActiveResultSets=true"
	 }
   }

4. Apply EF Core migrations (from the project folder containing the .csproj):

   dotnet ef database update

5. Run the API:

   dotnet run --project HotelListing.Api/HotelListing.Api.csproj

6. Open the API docs

   When running locally, Swagger UI is available at: https://localhost:{port}/swagger

## Projects & Packages
The API project uses these main packages (see csproj for exact versions):
- Microsoft.AspNetCore.OpenApi
- Microsoft.EntityFrameworkCore.SqlServer
- Microsoft.EntityFrameworkCore.Design
- Microsoft.OpenApi

## Development notes
- Target framework: .NET 10
- Keep packages up to date and run `dotnet restore` after changes to csproj

## Contributing
Feel free to open issues or pull requests. Follow the existing coding style and run the app/tests locally before submitting changes.

## License
This repository does not include an explicit license file. Add a LICENSE file if you intend to open-source the project.
