# RaceDay – Event Management Web Application

## 1. Project Overview

RaceDay is a web-based event management application developed to help organisers manage sporting events and allow participants to register for events, manage their enrolments and view their results.

The application provides a central platform where organisers and participants can access features according to their account roles. It was developed using ASP.NET Core MVC, ASP.NET Core Web API and SQL Server.

## 2. Project Objectives

The main objectives of RaceDay are to:

- Allow users to register and log in securely.
- Allow organisers to create, view, update and delete their events.
- Allow organisers to manage event categories.
- Allow participants to browse available events and enrol.
- Allow organisers to record and publish participant results.
- Allow participants to view their enrolments and published results.
- Allow users to view and update their profile information.
- Support profile photo uploads using Azure Blob Storage.

## 3. Technologies Used

The project uses the following technologies:

- C#
- ASP.NET Core 8 MVC
- ASP.NET Core Web API
- Entity Framework Core
- SQL Server and SQL Server LocalDB
- HTML5 and CSS3
- Bootstrap
- JavaScript
- Azure Blob Storage
- xUnit for automated testing
- Git and GitHub
- Docker (containerisation setup is still being completed)

## 4. System Structure

The RaceDay solution contains three main projects:

### RaceDay.Api
The API handles the application's business logic, database communication, authentication and data processing.

### RaceDay.Web
The MVC project provides the user interface. It communicates with the API using HTTP requests and displays information to organisers and participants.

### RaceDay.Tests
The test project contains automated tests used to check the application's functionality.

## 5. Main Features

### Authentication
- User registration.
- User login and logout.
- Session-based authentication.
- Organiser and participant roles.

### Organiser Features
- Organiser dashboard.
- Create, edit and delete events.
- Manage event categories.
- View participant enrolments.
- Record participant results.
- Publish and unpublish results.

### Participant Features
- View upcoming events.
- View event details and categories.
- Enrol in events.
- View personal enrolments.
- View published results.

### Profile Management
- View profile information.
- Update name and email address.
- Upload a profile photo using Azure Blob Storage.

## 6. Requirements

To run the application, the following software is required:

- Windows 10 or Windows 11.
- Visual Studio 2022.
- .NET 8 SDK.
- SQL Server LocalDB or a compatible SQL Server instance.
- Azure Storage Account for profile photo uploads.

## 7. How to Run the Application

### Step 1: Download the project

Clone the repository from GitHub or download the source code.

### Step 2: Open the solution

Open the RaceDay solution file in Visual Studio 2022.

### Step 3: Configure the database

Check the connection string named `RaceDayConnection` in the API project's `appsettings.json`.

Make sure SQL Server LocalDB is installed and available.

### Step 4: Update the database

Open the Package Manager Console in Visual Studio and select the `RaceDay.Api` project.

Run the following command if database migrations need to be applied:

```powershell
Update-Database
```

### Step 5: Configure Azure Blob Storage

Add your Azure Storage Account connection string and container name to the API configuration under the `AzureBlobStorage` section.

Do not upload passwords, connection strings or other secrets to GitHub.

### Step 6: Run the API

Set `RaceDay.Api` as a startup project and run it.

The development URLs are:

- HTTPS: `https://localhost:7024`
- HTTP: `http://localhost:5023`

### Step 7: Run the MVC application

Set `RaceDay.Web` as the startup project and run it.

Make sure the API is running so that the MVC application can communicate with it.

## 8. Automated Testing

The project includes an xUnit test project called `RaceDay.Tests`.

To execute the tests in Visual Studio:

1. Open Test Explorer.
2. Select Run All Tests.
3. Check that the tests pass.

The API test suite previously completed with eight passing tests.

## 9. Docker Support

Docker containerisation is part of the project requirements. The Dockerfile, container configuration and one-command startup instructions will be added and verified as part of the final deployment setup.

## 10. Future Improvements

Possible future improvements include:

- Improving the responsive design.
- Adding more event search and filtering options.
- Improving error handling and validation.
- Completing and testing Docker deployment.
- Expanding automated test coverage.

## 11. Conclusion

RaceDay provides a centralised platform for managing sporting events. It allows organisers to manage events and results while participants can discover events, enrol and track their progress.

The project demonstrates the use of ASP.NET Core MVC, Web API, database integration, cloud storage and automated software testing.
