# SpendSmart

SpendSmart is a web-based personal finance management application built with ASP.NET Core MVC. It allows users to manage their expenses, track spending, and maintain user accounts with secure authentication.

## Features

- **User Authentication**: Register, login, email verification, and password management using ASP.NET Identity.
- **Expense Tracking**: (Currently under development) Add, edit, view, and delete expenses.
- **Responsive UI**: Built with Bootstrap for a clean and responsive user interface.
- **Database Integration**: Uses Entity Framework Core with SQL Server for data persistence.

## Technologies Used

- **Backend**: ASP.NET Core 8.0 MVC
- **Database**: SQL Server (LocalDB for development)
- **ORM**: Entity Framework Core
- **Authentication**: ASP.NET Identity
- **Frontend**: Razor Views, Bootstrap, jQuery
- **Build Tool**: MSBuild

## Prerequisites

- .NET 8.0 SDK
- SQL Server (LocalDB is included with Visual Studio; otherwise, install SQL Server Express)
- Visual Studio 2022 or VS Code with C# extensions

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/rwandantechy/SpendSmart.git
   cd SpendSmart
   ```

2. **Restore NuGet packages**:
   ```bash
   dotnet restore
   ```

3. **Update database**:
   - Ensure SQL Server is running.
   - Run the migrations to set up the database:
     ```bash
     dotnet ef database update
     ```

4. **Build the project**:
   ```bash
   dotnet build
   ```

5. **Run the application**:
   ```bash
   dotnet run
   ```
   The application will be available at `https://localhost:5001` (or the port specified in `launchSettings.json`).

## Usage

- **Register**: Create a new account by providing your full name, email, and password.
- **Login**: Use your email and password to log in.
- **Verify Email**: If needed, verify your email for account recovery.
- **Change Password**: Update your password after verification.
- **Logout**: Securely log out of your account.

(Note: Expense management features are currently commented out and will be implemented in future updates.)

## Database Configuration

The application uses SQL Server with the connection string defined in `appsettings.json`:

```json
"ConnectionStrings": {
  "MySQLConnection": "Server=(localdb)\\MSSQLLocalDB;Database=SpendSmartOfficial;Trusted_Connection=True;MultipleActiveResultSets=true"
}
```

For production, update this to your SQL Server instance.

## Project Structure

- **Controllers**: Handle HTTP requests (AccountController for auth, HomeController for main pages).
- **Models**: Data models (Users inherits from IdentityUser).
- **ViewModels**: Models for views (Login, Register, etc.).
- **Views**: Razor views for UI.
- **Data**: DbContext and migrations.
- **wwwroot**: Static files (CSS, JS, Bootstrap).

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test thoroughly.
4. Submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For questions or support, please contact the repository owner.
