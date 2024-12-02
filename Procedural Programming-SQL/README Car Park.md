
# Parking System Database Project

## Overview
This project involves designing and normalizing a database for a parking system. The system tracks parking entry attempts, staff information, parking permits, and card swipes. The database is structured in compliance with normalization principles, ensuring data integrity and reducing redundancy.

## Features
- **Normalization**: Data is organized into 3NF and BCNF.
- **Tables**: Decomposed tables include Staff, Staff Card, Permit Reservation, Entry Attempt, and Parking Entry Information.
- **SQL Queries**: Includes queries for counting card swipes, listing staff with spot reservations, showing entry attempts for a specific card, calculating revenue, and more.

## Setup
To set up the database:
1. Create the tables as specified in the SQL schema.
2. Insert sample data into the tables using the provided SQL insert statements.

## Usage
Run the SQL queries to retrieve information such as:
- The number of swipe card records for each staff member.
- Staff with multiple parking reservations.
- Entry attempts for a specific card.
- Revenue and parking spot allocation statistics.

## Requirements
- MySQL or PostgreSQL database
- SQL query execution tools (e.g., MySQL Workbench, pgAdmin)
