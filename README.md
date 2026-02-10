<p align="center">
<img width="300" height="250" alt="selectallfromcar - Color" src="https://github.com/user-attachments/assets/490d41e5-fe27-435c-9a06-270aab570689" />
</p>

# Car Rental Management System (`CarBookingGroup37`)

PostgreSQL database schema for a **Car Rental Management System**. 

---

## Database Schema Overview

Three primary modules:

### 1. User & Authentication
* **`administator`**
* **`customer`**: Central table for user accounts, including unique driver's license linkage.
* **`logs`**: An audit trail of customer login/logout activity with boolean status.

### 2. Fleet & Shop Management
* **`car`**: Physical asset tracking (mileage, production year, plate number).
* **`car_info`**: Technical specifications and pricing (fuel type, transmission, price per day).
* **`shop`**: High-level shop data including operating hours and price ranges.
* **`shop_desc`**: Detailed location data (address, district, province, and postal code).

### 3. Rental Transactions
* **`Rental`**: The core operational table. It bridges customers, cars, and shops.
    * Tracks pickup/return dates and locations (Pickup Shop vs. Return Shop).
    * Mileage usage (`mileage_start` to `mileage_end`).
    * Discounts and Daily rates.

---

## Setup

### Prerequisites
* PostgreSQL 18 or higher installed.
* An SQL client (pgAdmin, DBeaver, or command line).

### Installation
1. **Create the Database:**
   ```sql
   CREATE DATABASE "CarBookingGroup37";
2. **Import the Schema: Using the terminal:**
   ```sql
   psql -U your_username -d CarBookingGroup37 -f CarBookingGroup37.sql
   
---

### ERD diagram 
<img width="1634" height="917" alt="ERD Diagram from Pgadmin" src="https://github.com/user-attachments/assets/faa86517-5fa0-429b-80ff-7dc1b88b8e94" />
