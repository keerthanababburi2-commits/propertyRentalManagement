<<<<<<< HEAD
# Property Rental Management Platform (MySQL)

A full-stack starter project based on your architecture diagram. It uses **React + Vite**, **Spring Boot**, and **MySQL** (not PostgreSQL).

## Features included
- Responsive React dashboard with property search and filters
- Property listing cards with rent, location, type, bedrooms and availability
- Property CRUD REST API
- Rental application submission and application status tracking
- Dashboard statistics for total properties, available properties, applications and monthly rent
- MySQL schema and sample data
- Image URL support for property photos
- Admin-ready backend structure; demo payment endpoint is clearly marked as simulated

## Requirements
- Java 17+
- Maven 3.9+
- Node.js 20+
- MySQL 8+

## 1. Create the database
Open MySQL Workbench or MySQL command line and run:

```sql
CREATE DATABASE property_rental_db;
```

The backend also creates tables automatically on startup with `spring.jpa.hibernate.ddl-auto=update`.

## 2. Configure MySQL
Edit `backend/src/main/resources/application.properties` or set environment variables:
- `DB_URL` (default `jdbc:mysql://localhost:3306/property_rental_db`)
- `DB_USERNAME` (default `root`)
- `DB_PASSWORD` (set your local MySQL password)

Windows CMD example:
```cmd
set DB_USERNAME=root
set DB_PASSWORD=your_mysql_password
cd backend
mvn spring-boot:run
```

## 3. Run backend
```cmd
cd backend
mvn spring-boot:run
```
API base URL: `http://localhost:8080/api`

## 4. Run frontend
Open a second terminal:
```cmd
cd frontend
npm install
npm run dev
```
Open the Vite URL shown in the terminal (usually `http://localhost:5173`).

## Main API endpoints
- `GET /api/properties` — list properties; optional `search`, `city`, `type`, `maxRent`
- `GET /api/properties/{id}` — property details
- `POST /api/properties` — create property
- `PUT /api/properties/{id}` — update property
- `DELETE /api/properties/{id}` — delete property
- `GET /api/applications` — list applications
- `POST /api/applications` — apply to rent a property
- `PATCH /api/applications/{id}/status?status=APPROVED` — update status
- `GET /api/dashboard/stats` — dashboard summary
- `POST /api/payments/demo` — simulated payment record (no real money is charged)

## Notes
This is a student-project starter, not a production payment/authentication system. The payment endpoint is a demo only. Before public deployment, add proper authentication/authorization, validation, secure image upload storage, migrations, and a real payment provider integration.
=======
# propertyRentalManagement
>>>>>>> 572e80339d77a750a839d70047fe2c5b47e18388
