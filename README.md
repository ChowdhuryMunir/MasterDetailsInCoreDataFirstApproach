# MasterDetailsInCoreDataFirstApproach

`MasterDetailsInCoreDataFirstApproach` is a sample ASP.NET Core application demonstrating a "Master-Details" design pattern using Entity Framework Core with a "Data-First" approach. This project provides a structured way to handle master-detail relationships and data management within a .NET Core application.

## Features

- **Master-Detail Relationship:** Manages relationships between master and detail entities effectively.
- **Data-First Approach:** Utilizes an existing database schema to generate Entity Framework models.
- **CRUD Operations:** Implements create, read, update, and delete operations for both master and detail entities.
- **Entity Framework Core Integration:** Leverages EF Core for ORM capabilities and database interactions.

## Getting Started

To set up and run the project locally, follow these steps:

### Prerequisites

Ensure you have the following installed:

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) or any compatible database

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ChowdhuryMunir/MasterDetailsInCoreDataFirstApproach.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd MasterDetailsInCoreDataFirstApproach
   ```

3. **Install dependencies:**

   The project dependencies are managed via NuGet. Restore them using:

   ```bash
   dotnet restore
   ```

4. **Update the connection string:**

   Edit the `appsettings.json` file to include your database connection string:

   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=your_server;Database=your_database;User Id=your_user;Password=your_password;"
   }
   ```

5. **Apply database migrations (if applicable):**

   If there are any pending migrations, apply them using:

   ```bash
   dotnet ef database update
   ```

6. **Run the application:**

   Start the application using:

   ```bash
   dotnet run
   ```

   The application will be available at `http://localhost:5000` (or the port specified in `launchSettings.json`).

## Project Structure

- **Models:** Contains the entity classes generated from the existing database schema.
- **Data:** Includes the `DbContext` and configuration for Entity Framework Core.
- **Controllers:** Implements API endpoints or MVC controllers for handling requests.
- **Views:** Contains Razor views for displaying data (if using MVC).
- **wwwroot:** Static files like CSS, JavaScript, and images.

## API Endpoints

### Master Entity Endpoints

- **GET** `/api/master` - Retrieve a list of master entities.
- **POST** `/api/master` - Create a new master entity.
- **GET** `/api/master/{id}` - Retrieve a specific master entity by ID.
- **PUT** `/api/master/{id}` - Update a master entity.
- **DELETE** `/api/master/{id}` - Delete a master entity.

### Detail Entity Endpoints

- **GET** `/api/detail` - Retrieve a list of detail entities.
- **POST** `/api/detail` - Create a new detail entity.
- **GET** `/api/detail/{id}` - Retrieve a specific detail entity by ID.
- **PUT** `/api/detail/{id}` - Update a detail entity.
- **DELETE** `/api/detail/{id}` - Delete a detail entity.

## Usage

You can use tools like [Postman](https://www.postman.com/downloads/) or [curl](https://curl.se/) to interact with the API endpoints. For example, to get a list of master entities:

```http
GET /api/master
```

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push the branch (`git push origin feature/your-feature`).
5. Open a pull request describing your changes.

Please refer to our [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

## License

This project is licensed under the [MIT License](LICENSE). See the [LICENSE](LICENSE) file for more information.

## Contact

For questions or feedback, please contact [MunirchowdhurySaif](mailto:munir.idb@gmail.com.com).

---
