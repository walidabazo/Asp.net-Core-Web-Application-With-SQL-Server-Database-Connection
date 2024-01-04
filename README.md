# Asp.net-Core-Web-Application-With-SQL-Server-Database-Connection
Asp.net Core 8 Web Application With SQL Server Database Connection

[![Watch the video](https://img.youtube.com/vi/TmocySu6xiM/0.jpg)](https://youtu.be/TmocySu6xiM)

## Visual Studio 2022 download
## Create New ASP.NET Core Project
## Create Asp.Net Core models
## Create Asp.Net Core models
      public class Emplyee
       {
         public int Id { get; set; }
         public string FirestName { get; set; }
         public string MiddleName { get; set; }
         public string LastName { get; set; }
         public string EmailAddress { get; set; }
         public int PhoneNo { get; set; }
       }

## Create Database and Table MS SQL Server
## Install Nugets ASP.NET Core ( Entity Framework )
## Create Application Db Context Class
        public class ApplicationDbContext : DbContext
         {
            public ApplicationDbContext(DbContextOptions<ApplicationDbContext> contextOptions) : base(contextOptions)  { } 
            public DbSet<Emplyee> Emplyees { get; set; }
         }
## Configure SQL Database Connection on appsettings.json file
       "ConnectionStrings": {
                     "DefualtConnection": "Data Source=.;Initial Catalog=company;Integrated Security=True;Trust Server Certificate=True"
                            },
## Register Database Connections on  class
      builder.Services.AddDbContext<ApplicationDbContext>(options =>
       {
         options.UseSqlServer(builder.Configuration.GetConnectionString("DefualtConnection"));
       });
## Add-Migrations ASP.NET Core
## Update-Database (Apply Migrations) Asp.Net Core
## Scaffolding in Asp.Net Core
## CRUD Operation
## Add Fontawsome in Asp.Net Core Application
