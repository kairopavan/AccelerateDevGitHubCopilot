# Library App

## Description
Library App is a console-based library management system designed to manage patrons, books, and loans. It features a multi-layered architecture with a clear separation of concerns, making it easy to maintain and extend.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`
- `README.md`
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
    - `Library.ApplicationCore.csproj`
  - `Library.Console/`
    - `appSettings.json`
    - `CommonActions.cs`
    - `ConsoleApp.cs`
    - `ConsoleState.cs`
    - `Json/`
    - `Library.Console.csproj`
    - `Program.cs`
  - `Library.Infrastructure/`
    - `Data/`
    - `Library.Infrastructure.csproj`
- `tests/`
  - `UnitTests/`
    - `ApplicationCore/`
    - `UnitTests.csproj`

## Key Classes and Interfaces
- **Library.ApplicationCore**
  - `Entities/`
    - `Patron`: Represents a library patron.
    - `Loan`: Represents a loan of a book to a patron.
  - `Enums/`
    - `ConsoleState`: Enum representing the different states of the console application.
  - `Interfaces/`
    - `IPatronRepository`: Interface for patron data access.
    - `ILoanRepository`: Interface for loan data access.
    - `ILoanService`: Interface for loan-related business logic.
    - `IPatronService`: Interface for patron-related business logic.
  - `Services/`
    - `LoanService`: Implements `ILoanService`.
    - `PatronService`: Implements `IPatronService`.

- **Library.Console**
  - `ConsoleApp`: Main class for running the console application.
  - `Program`: Entry point of the console application.
  - `CommonActions`: Enum representing common actions in the console application.
  - `ConsoleState`: Enum representing the different states of the console application.

- **Library.Infrastructure**
  - `Data/`
    - `JsonPatronRepository`: Implements `IPatronRepository` for JSON data.
    - `JsonLoanRepository`: Implements `ILoanRepository` for JSON data.
    - `JsonData`: Provides methods to load and save data to JSON files.

## Usage
1. Clone the repository.
2. Open the solution file `AccelerateDevGitHubCopilot.sln` in Visual Studio.
3. Build the solution to restore dependencies and compile the code.
4. Run the `Library.Console` project to start the console application.

## License
This project is licensed under the MIT License.
