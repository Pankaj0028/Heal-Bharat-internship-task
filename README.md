# Heal-Bharat-internship-task

Travel Booking System Database

This repository contains the SQL database schema and sample data for a travel booking system. The database is designed to manage users, destinations, bookings, and payments for a travel application.

## Database Schema

The database consists of four main tables:

1. `users` - Stores user information including credentials and roles
2. `destinations` - Contains travel destination details with pricing
3. `bookings` - Tracks user bookings for destinations
4. `payments` - Records payment transactions for bookings

## Files Included

- **SQL Schema File:**
  - `code.sql` - Complete SQL script to create the database schema and populate with sample data

- **CSV Data Files:**
  - `users.csv` - Contains 4 sample user records (1 admin, 3 regular users)
  - `destinations.csv` - Contains 5 popular travel destinations with details
  - `bookings.csv` - Contains 3 sample booking records with different statuses
  - `payments.csv` - Contains 2 completed payment records

## Installation Instructions

To set up this database:

1. Create a MySQL database
2. Run the `code.sql` script to:
   - Create all tables with proper relationships
   - Insert all sample data from the CSV files
3. Alternatively, you can import the individual CSV files into your database management system

## File Details

### `code.sql`
- Creates all database tables with proper constraints
- Includes foreign key relationships between tables
- Inserts all sample data that matches the CSV files
- Contains sample queries to view the data

### `users.csv`
- Columns: `user_id, username, email, password_hash, full_name, role, created_at`
- Contains:
  - 1 admin user (admin_user)
  - 3 regular users (john_doe, jane_smith, travel_bug)
- All passwords are hashed (placeholder values)

### `destinations.csv`
- Columns: `destination_id, name, location, description, price_per_night, image_url, created_at`
- Contains 5 luxury destinations:
  - Eiffel Tower Suite (Paris)
  - Kyoto Serenity Garden (Japan)
  - Santorini Caldera View (Greece)
  - NYC Times Square Loft (USA)
  - Bora Bora Overwater Bungalow (French Polynesia)

### `bookings.csv`
- Columns: `booking_id, user_id, destination_id, check_in_date, check_out_date, total_price, status, created_at`
- Contains 3 bookings:
  - 2 confirmed bookings
  - 1 pending booking

### `payments.csv`
- Columns: `payment_id, booking_id, amount, payment_method, status, payment_date`
- Contains 2 completed payments:
  - 1 Credit Card payment
  - 1 PayPal payment

## Sample Queries

The SQL script includes basic SELECT queries to view all data in each table:

```sql
SELECT * FROM users;
SELECT * FROM destinations;
SELECT * FROM bookings;
SELECT * FROM payments;
```

## Important Notes

- All password hashes in the sample data are placeholder values and should be replaced in production
- All timestamps in the sample data are set to "2025-08-08 17:14:45" for consistency
- The database schema includes proper foreign key constraints between tables
- Image URLs in destinations are example.com placeholders
-
