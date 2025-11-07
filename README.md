# EduTrack - .NET Scaffold (Expanded UI + EF guidance)

This repository is an expanded scaffold for EduTrack — a student performance tracking system built with ASP.NET Core 8 and EF Core.

## What was added in this expansion (Option A)
- Full Razor Pages CRUD for Students (Index, Create, Edit, Details, Delete)
- Admin Dashboard page with Chart.js demo (students per grade)
- Student API controller with full CRUD
- `scripts/init_database.sql` — a SQL Server schema script for quick DB provisioning
- Updated `README` with instructions to create EF migrations locally

## Quick start (local)
1. Install .NET 8 SDK.
2. From the project root run:
   ```bash
   cd EduTrack.Web
   dotnet restore
   dotnet tool install --global dotnet-ef
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   dotnet run
   ```

If you cannot run `dotnet ef migrations` on your machine, use the `scripts/init_database.sql` against your SQL Server instance to create core tables. Note that ASP.NET Identity needs its own tables — recommended approach is to run `dotnet ef database update`.

## Default seed user
- Admin: `admin@edutrack.local` / `P@ssw0rd!`

## Next recommendations
- Add Razor CRUD pages for Teachers, Subjects, Grades, Attendance, Assignments (similar to Students pages)
- Secure pages with role-based authorization
- Add paging/search to list pages
- Integrate Chart.js or a server-side charting library for richer analytics

