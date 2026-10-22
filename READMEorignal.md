# 💜 InternTrack — Internship Application Tracker

A web-based application built with **ASP.NET Core MVC and MySQL** to help students organize, track, and manage their internship applications in one place.

## 📌 About the Project

Applying for multiple internships can become difficult to manage. InternTrack provides a centralized dashboard where students can record internship opportunities, monitor application statuses, and keep important application details organized.

## ✨ Features

- 📊 **Dashboard** — View total applications, submitted applications, interviews, and selections.
- ➕ **Add Internship** — Save company names, job roles, application links, locations, deadlines, and other details.
- ✏️ **Edit Applications** — Update saved application information.
- 🗑️ **Delete Applications** — Remove applications you no longer need.
- 📋 **Application Tracker** — View your saved internship applications.
- 🎨 **Clean User Interface** — Responsive layout with a purple-themed navigation bar and dashboard cards.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| C# | Application programming language |
| ASP.NET Core MVC (.NET 8) | Web application framework |
| Entity Framework Core | Database access and ORM |
| MySQL | Relational database |
| Bootstrap | Responsive UI styling |
| HTML and CSS | Page structure and design |
| JavaScript | Client-side interactions |
| Git and GitHub | Version control and project hosting |

## 🏗️ System Architecture

InternTrack follows the **Model–View–Controller (MVC)** pattern.

```text
             User / Browser
                    |
                    v
             MVC Controllers
                    |
          +---------+---------+
          |                   |
          v                   v
        Models              Views
          |              (Razor / HTML)
          |
          v
    Entity Framework Core
          |
          v
        MySQL DB
```

- **Model:** Represents internship application data.
- **View:** Displays the dashboard, application list, and forms.
- **Controller:** Handles user requests and application operations.
- **Database:** Stores internship application records in MySQL.

## 📂 Project Structure

```text
InternTrack/
├── Controllers/
│   ├── HomeController.cs
│   └── InternshipApplicationsController.cs
├── Data/
│   └── ApplicationDbContext.cs
├── Migrations/
├── Models/
│   ├── ErrorViewModel.cs
│   └── InternshipApplication.cs
├── Views/
│   ├── Home/
│   ├── InternshipApplications/
│   │   ├── Dashboard.cshtml
│   │   ├── Index.cshtml
│   │   ├── Create.cshtml
│   │   └── Edit.cshtml
│   └── Shared/
├── wwwroot/
│   ├── css/
│   ├── js/
│   └── lib/
├── Program.cs
├── appsettings.json
├── InternTrack.csproj
└── README.md
```

## ⚙️ Getting Started

### Prerequisites

Install the following:

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [MySQL](https://dev.mysql.com/downloads/)
- [Git](https://git-scm.com/downloads)
- Visual Studio Code or another compatible editor

### 1. Clone the repository

```bash
git clone https://github.com/saminabilakhia/InternTrack.git
cd InternTrack
```

### 2. Restore dependencies

```bash
dotnet restore
```

### 3. Configure the database

Create a MySQL database named `interntrack_db` if it does not already exist.

Configure the connection string using **.NET User Secrets** rather than committing passwords to GitHub.

For example, from the project directory:

```bash
dotnet user-secrets init
dotnet user-secrets set "ConnectionStrings:DefaultConnection" "YOUR_CONNECTION_STRING"
```

Replace `YOUR_CONNECTION_STRING` with your own MySQL connection string, including your local database username and password.

> Keep your credentials private. Never commit passwords, API keys, or other secrets to source control.

### 4. Apply database migrations

If the database tables have not already been created, run:

```bash
dotnet tool install --global dotnet-ef --version 8.0.8
dotnet ef database update
```

If the tool is already installed, you can skip the installation command.

### 5. Run the application

```bash
dotnet run
```

Open the local URL displayed in your terminal.

## 📸 Application Screenshots

Screenshots of the Dashboard, Applications page, and Create/Edit forms can be added here as the project evolves.

For example, save screenshots in a folder named `screenshots` and reference them like this:

```markdown
![InternTrack Dashboard](screenshots/dashboard.png)
![InternTrack Applications](screenshots/applications.png)
```

## 🎯 Project Objectives

- Simplify internship application tracking.
- Keep application details organized in one place.
- Monitor application progress and interview opportunities.
- Practice ASP.NET Core MVC, database integration, and responsive UI development.

## 🚀 Future Improvements

- Search and filter internship applications.
- Deadline reminders and notifications.
- Application analytics and progress charts.
- Export application records to CSV or PDF.

## 👩‍💻 Author

**Samina Bilakhia**

Computer Science and Engineering Student

[GitHub Profile](https://github.com/saminabilakhia)

---

*Built as a learning project to practice full-stack web development with ASP.NET Core MVC and MySQL.*
