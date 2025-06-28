# 🏨 Hotel Management System

A comprehensive hotel management solution built with .NET 5, featuring both web and desktop applications for efficient hotel operations.

![.NET 5](https://img.shields.io/badge/.NET-5.0-512BD4?style=for-the-badge&logo=.net&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-512BD4?style=for-the-badge&logo=aspnet&logoColor=white)
![WPF](https://img.shields.io/badge/WPF-512BD4?style=for-the-badge&logo=windows&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

## 🎯 Overview

The Hotel Management System is a full-featured application designed to streamline hotel operations including room booking, guest management, check-ins, and room availability tracking. The solution consists of:

- **Web Application**: Modern ASP.NET Core web interface for online bookings
- **Desktop Application**: WPF-based desktop application for hotel staff
- **Shared Library**: Common business logic and data access layer
- **Database**: SQL Server database with stored procedures

## ✨ Features

### 🌐 Web Application

- **Room Search**: Browse available rooms with filtering options
- **Online Booking**: Secure room reservation system
- **Responsive Design**: Modern UI that works on all devices
- **Real-time Availability**: Live room status updates

### 💻 Desktop Application

- **Guest Check-in**: Streamlined check-in process
- **Room Management**: Comprehensive room status tracking
- **Booking Management**: View and manage all reservations
- **Staff Interface**: Intuitive interface for hotel staff

### 🗄️ Database Features

- **Stored Procedures**: Optimized database operations
- **Data Integrity**: Proper relationships and constraints
- **Scalable Design**: Efficient data structure for growth

## 🏗️ Architecture

The application follows a clean architecture pattern with clear separation of concerns:

```
HotelApp/
├── HotelApp.Web/          # ASP.NET Core Web Application
├── HotelApp.Desktop/      # WPF Desktop Application
├── HotelAppLibrary/       # Shared Business Logic & Data Access
└── HotelAppDB/           # SQL Server Database Project
```

### Key Components

- **Models**: Data transfer objects for business entities
- **Data Access**: Dapper-based data access layer
- **Stored Procedures**: Database operations for performance
- **Dependency Injection**: Modern .NET DI container usage

## 🔧 Prerequisites

Before running this application, ensure you have the following installed:

- **.NET 5.0 SDK** or later
- **Visual Studio 2019/2022** or **Visual Studio Code**
- **SQL Server** (2016 or later) or **SQL Server Express**
- **SQL Server Management Studio** (SSMS) for database management

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/hotelapp.git
cd hotelapp
```

### 2. Restore Dependencies

```bash
dotnet restore
```

### 3. Build the Solution

```bash
dotnet build
```

## 🗄️ Database Setup

### 1. Database Creation

1. Open **SQL Server Management Studio**
2. Connect to your SQL Server instance
3. Right-click on **Databases** → **New Database**
4. Name it `HotelAppDB`

### 2. Deploy Database Schema

1. Open the `HotelAppDB` project in Visual Studio
2. Right-click on the project → **Publish**
3. Configure your connection string
4. Click **Publish** to deploy the database

### 3. Update Connection Strings

Update the connection strings in the following files:

**Web Application** (`HotelApp.Web/appsettings.json`):

```json
{
  "ConnectionStrings": {
    "Default": "Server=YOUR_SERVER;Database=HotelAppDB;Trusted_Connection=true;"
  }
}
```

**Desktop Application** (`HotelApp.Desktop/appsettings.json`):

```json
{
  "ConnectionStrings": {
    "Default": "Server=YOUR_SERVER;Database=HotelAppDB;Trusted_Connection=true;"
  }
}
```

## 💻 Usage

### Running the Web Application

```bash
cd HotelApp.Web
dotnet run
```

The web application will be available at `https://localhost:5001`

### Running the Desktop Application

```bash
cd HotelApp.Desktop
dotnet run
```

Or open the solution in Visual Studio and run the `HotelApp.Desktop` project.

## 📁 Project Structure

```
HotelApp/
├── HotelApp.Web/                 # Web Application
│   ├── Pages/                   # Razor Pages
│   │   ├── BookRoom.cshtml      # Room booking page
│   │   ├── RoomSearch.cshtml    # Room search page
│   │   └── Shared/              # Shared layouts
│   ├── wwwroot/                 # Static files
│   └── Program.cs               # Application entry point
├── HotelApp.Desktop/            # Desktop Application
│   ├── MainWindow.xaml          # Main application window
│   ├── CheckInForm.xaml         # Check-in form
│   └── App.xaml                 # Application configuration
├── HotelAppLibrary/             # Shared Library
│   ├── Models/                  # Data models
│   ├── Data/                    # Data access layer
│   └── Databases/               # Database utilities
└── HotelAppDB/                  # Database Project
    ├── Tables/                  # Database tables
    └── Stored Procedures/       # Database procedures
```

## 🛠️ Technologies Used

### Backend

- **.NET 5.0** - Cross-platform development framework
- **ASP.NET Core** - Web application framework
- **WPF** - Desktop application framework
- **Dapper** - Micro ORM for data access
- **SQL Server** - Relational database

### Frontend

- **Razor Pages** - Server-side web pages
- **Bootstrap** - CSS framework for responsive design
- **jQuery** - JavaScript library
- **XAML** - UI markup language for WPF

### Development Tools

- **Visual Studio** - Integrated development environment
- **SQL Server Management Studio** - Database management
- **Git** - Version control

<div align="center">
  <sub>Built with .NET 5 • ASP.NET Core • WPF • SQL Server</sub>
</div>
