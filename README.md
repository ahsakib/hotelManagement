

```markdown
# Hotel Management System

![Java](https://img.shields.io/badge/Java-17-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![Swing](https://img.shields.io/badge/Java%20Swing-GUI-green)

A **Hotel Management System** built using Java and MySQL to manage hotel operations efficiently. This system provides a user-friendly interface for handling room bookings, customer details, and revenue tracking.

---

## Features
- **Dashboard**: Displays key metrics like total rooms, customers, revenue, and recent bookings.
- **Room Management**: Add, update, and manage room details.
- **Customer Management**: Store and manage customer information.
- **Booking Management**: Handle room bookings and check-ins/check-outs.
- **Revenue Tracking**: Monitor total revenue generated from bookings.
- **User Authentication**: Secure login and logout functionality.

---

## Technologies Used
- **Front-end**: Java Swing
- **Back-end**: MySQL
- **Database**: MySQL Database for storing room, customer, and booking details.
- **Tools**: IntelliJ IDEA, MySQL Workbench

---

## Database Schema

The database consists of the following tables:

### 1. `booking`
Stores information about room bookings.
```sql
CREATE TABLE `booking` (
  `id` int(11) NOT NULL,
  `room` int(11) DEFAULT NULL,
  `customer` int(11) DEFAULT NULL,
  `booking_date` varchar(50) DEFAULT NULL,
  `duration` int(11) DEFAULT NULL,
  `cost` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```

### 2. `customer`
Stores customer details.
```sql
CREATE TABLE `customer` (
  `id` int(11) NOT NULL,
  `name` varchar(100) DEFAULT NULL,
  `phone` varchar(50) DEFAULT NULL,
  `gender` varchar(50) DEFAULT NULL,
  `address` varchar(200) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```

### 3. `room`
Stores room details.
```sql
CREATE TABLE `room` (
  `id` int(11) NOT NULL,
  `name` varchar(100) DEFAULT NULL,
  `number` int(11) DEFAULT NULL,
  `type` varchar(50) DEFAULT NULL,
  `status` varchar(30) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```

### 4. `users`
Stores user login credentials.
```sql
CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `username` varchar(50) NOT NULL,
  `password` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```

---

## Sample Data for `users` Table
The `users` table contains the following sample data for login:

| id  | username | password  |
|-----|----------|-----------|
| 1   | admin    | admin123  |

**Default Login Credentials:**
- **Username**: `admin`
- **Password**: `admin123`

---

## Installation and Setup

### Prerequisites
- Java Development Kit (JDK) 17 or higher
- MySQL Server 8.0 or higher
- MySQL Connector/J (for Java-MySQL connectivity)

### Steps to Run the Project
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/hotel-management-system.git
   cd hotel-management-system
   ```

2. **Set Up the Database**:
   - Open MySQL Workbench or any MySQL client.
   - Create a new database named `HotelManagement`.
   - Import the SQL file (`hotel_management.sql`) located in the `database` folder to set up the required tables.

3. **Configure Database Connection**:
   - Open the `DBConnection.java` file.
   - Update the database URL, username, and password with your MySQL credentials.

4. **Run the Application**:
   - Open the project in IntelliJ IDEA or any Java IDE.
   - Build and run the `Dashboard.java` file to start the application.

---

## Screenshots

### Dashboard
![Dashboard](screenshots/dashboard.png)

### Room Management
![Room Management](screenshots/room_management.png)

### Customer Management
![Customer Management](screenshots/customer_management.png)

### Booking Management
![Booking Management](screenshots/booking_management.png)

---

## Contributing
Contributions are welcome! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact
For any questions or feedback, feel free to reach out:
- **Name**: Your Name
- **Email**: your.email@example.com
- **GitHub**: [your-username](https://github.com/your-username)

---
```

---

### How to Use:
1. Replace placeholders like `your-username`, `your.email@example.com`, and `Your Name` with your actual details.
2. Add screenshots of your application to the `screenshots` folder and update the paths in the README.md file.
3. Push the updated README.md file to your GitHub repository.

This README.md file will provide a clear and professional overview of your project, including the database schema and login credentials for testing.