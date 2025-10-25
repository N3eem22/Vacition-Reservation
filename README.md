# 🏖️ WhiteLagoon – Vacation Reservation System

A Clean Architecture ASP.NET MVC application for managing villa bookings, payments, and amenities.

## 🧭 Overview
**WhiteLagoon** is a layered ASP.NET Core 8.0 web application following **Clean Architecture** principles.
It separates responsibilities across four projects:
1. **Domain** – core entities and business rules.
2. **Application** – service layer, business logic, interfaces.
3. **Infrastructure** – EF Core, repositories, email, Stripe, and persistence.
4. **Web (UI)** – MVC presentation, controllers, and views.

The app supports villa listings, amenities, booking flow with Stripe payments, and email notifications via SendGrid.

## ⚙️ Features
- 🏠 CRUD management for Villas and Amenities  
- 🧾 Booking flow with Stripe checkout session  
- 📬 Automatic email confirmation via SendGrid  
- 🔐 ASP.NET Identity-based authentication & authorization  
- 📊 Admin Dashboard (via IDashboardService)  
- 🧱 Clean Architecture with Repository + Unit of Work pattern  
- 🌐 EF Core 8 (SQL Server) with code-first migrations  
- 💄 Bootstrap/jQuery-based UI

## ⚙️ Setup & Configuration
### Prerequisites
- .NET 8 SDK  
- SQL Server  
- Stripe account (for test payments)  
- SendGrid API key  
- Syncfusion license (optional, used for UI components)

### Configuration
Set up `appsettings.json` (see sample):

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=.;Database=WhiteLagoon;Trusted_Connection=True;TrustServerCertificate=True"
  },
  "Stripe": {
    "SecretKey": "your_stripe_secret",
    "PublishableKey": "your_stripe_public"
  },
  "SendGrid": {
    "Key": "your_sendgrid_key"
  },
  "Syncfusion": {
    "LicenseKey": "your_syncfusion_license"
  }
}
```

### Database Initialization
```bash
dotnet ef database update --project WhiteLagoon.Infrastructure --startup-project WhiteLagoon.Web
```

### Run the Application
```bash
dotnet run --project WhiteLagoon.Web
```
Browse to `https://localhost:5001`.

## 🤝 Contributing
1. Fork the repo  
2. Create a branch (`feature/reservation-cancellation`)  
3. Commit and push  
4. Submit a Pull Request


