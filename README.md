# ContosoPizza

A full-stack ASP.NET Core Razor Pages web application for managing a pizza menu, built with .NET 7 and Entity Framework Core.

## What It Does

- Browse a list of pizzas with details like name, size, gluten-free status, and price
- Add new pizzas to the menu
- Delete pizzas from the menu
- Persistent storage using SQLite via Entity Framework Core

## Tech Stack

- **Framework:** ASP.NET Core 7.0 (Razor Pages)
- **Language:** C#
- **Database:** SQLite with Entity Framework Core
- **Frontend:** Razor Views, Bootstrap, jQuery
- **ORM:** Entity Framework Core 7.0

## Project Structure

```
ContosoPizza/
├── ContosoPizza.csproj       # Project file targeting .NET 7
├── ContosoPizza.sln          # Solution file
├── Program.cs                # App entry point and service configuration
├── Data/
│   └── PizzaContext.cs       # EF Core DbContext for Pizza
├── Models/
│   └── Pizza.cs              # Pizza model with validation attributes
├── Services/
│   └── PizzaService.cs       # Business logic for CRUD operations
├── Pages/
│   ├── Index.cshtml          # Main page displaying pizza list
│   ├── Index.cshtml.cs       # Index page model
│   ├── Privacy.cshtml        # Privacy policy page
│   ├── Error.cshtml          # Error page
│   └── Shared/               # Shared layouts and partials
├── Migrations/               # EF Core database migrations
└── wwwroot/                  # Static files (CSS, JS, libs)
```

## Getting Started

### Prerequisites

- [.NET 7 SDK](https://dotnet.microsoft.com/download/dotnet/7.0)
- SQLite (included via NuGet package)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Aaryan018/Practice.git
   cd Practice
   ```

2. Restore dependencies:
   ```bash
   dotnet restore
   ```

3. Apply database migrations:
   ```bash
   dotnet ef database update
   ```

4. Run the application:
   ```bash
   dotnet run
   ```

5. Open your browser to `https://localhost:5001` (or the URL shown in the terminal).

## Features

- Create, read, and delete pizza entries
- Form validation for pizza properties (name required, price range validation)
- SQLite database with EF Core migrations
- Responsive UI with Bootstrap
