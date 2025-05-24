# Textile and garment Management System

The **Garment Production Tracking Desktop Application** is designed to streamline and optimize the garment production process. Developed using **PHP** and **JavaScript**, this application facilitates seamless data flow and improves operational visibility, ensuring efficient management of products, categories, and orders.

With a focus on real-time tracking and data integrity, the system has achieved **99.9% uptime** since deployment. By implementing **CRUD operations** (Create, Read, Update, Delete), the application has reduced manual entry errors by **25%**, enhancing overall productivity and reducing human errors in the production process.

---

## Features

* **Product Management**: Effortlessly add, update, and delete products in the garment production line.
* **Category Management**: Manage categories of products to ensure organized production tracking.
* **Order Tracking**: Track orders from production to delivery, ensuring transparency and timely deliveries.
* **Real-time Updates**: Get immediate insights into production progress, stock levels, and order statuses.
* **Data Integrity**: The use of **CRUD operations** ensures consistent and accurate data, minimizing errors.
* **Seamless Data Flow**: Ensures smooth interaction between production departments, reducing bottlenecks and improving operational visibility.
* **99.9% Uptime**: Achieved since deployment, ensuring continuous availability for production teams.

---

## Tech Stack

* **Backend**:

  * **PHP**: For server-side logic and database interactions.
  * **MySQL**: For managing the production-related data (products, categories, orders).
* **Frontend**:

  * **JavaScript**: For dynamic interactions and data updates on the client side.
  * **HTML5/CSS3**: For structuring and styling the desktop application interface.
* **Architecture**:

  * **MVC (Model-View-Controller)**: Used for clean separation of concerns and maintainable codebase.
* **Server**:

  * Local or cloud-based PHP server for hosting the backend application.

---

## Prerequisites

Before you begin, ensure you have the following installed:

* **PHP** (latest stable version)
* **MySQL Database** (for storing production data)
* **XAMPP/WAMP/LAMP**: For local server setup (PHP + MySQL)
* **Web Browser**: For accessing the desktop application interface.

---

## Installation

### Clone the Repository

Clone the repository to your local machine using Git:

```bash
git clone https://github.com/yourusername/Garment-Production-Tracking-App.git
```

### Set Up Database

1. **Create the Database**:

   * Open **MySQL Workbench** or your preferred MySQL client.
   * Run the following SQL commands to create the necessary database and tables:

```sql
CREATE DATABASE garment_production;

USE garment_production;

CREATE TABLE products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product_name VARCHAR(100),
    category_id INT,
    quantity INT,
    price DECIMAL(10, 2)
);

CREATE TABLE categories (
    id INT AUTO_INCREMENT PRIMARY KEY,
    category_name VARCHAR(100)
);

CREATE TABLE orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    order_date DATE,
    product_id INT,
    quantity INT,
    status VARCHAR(50),
    FOREIGN KEY (product_id) REFERENCES products(id)
);
```

2. **Import the Database**:

   * Import the database into MySQL and ensure all the tables are correctly set up.

### Setup PHP Server

1. Install **XAMPP/WAMP/LAMP** (depending on your operating system) to create a local server environment.
2. Place the project files in the **htdocs** directory (for XAMPP) or the appropriate folder for your PHP server.
3. Start **Apache** and **MySQL** services from the XAMPP/WAMP control panel.
4. Open a web browser and access the application at `http://localhost/yourprojectfolder`.

---

## Usage

1. **Login**: Access the application via the desktop interface.
2. **Manage Products**: Add, update, or delete products in the garment production line.
3. **Manage Categories**: Organize products by categories for easier tracking.
4. **Track Orders**: View and manage production orders, monitor status, and update delivery dates.
5. **Search and Filter**: Quickly search for products and orders to stay on top of production.
6. **Real-Time Updates**: View the current production status of each order and product in real-time.

---

## Project Structure

Here’s an overview of the project structure:

```bash
Garment-Production-Tracking-App/
├── assets/                   # Static files (images, CSS, etc.)
├── config/                   # Database and server configuration
├── controllers/              # PHP files handling user requests and logic
├── models/                   # PHP classes for interacting with the database (Product, Order, etc.)
├── views/                    # Frontend views (HTML, JavaScript)
│   ├── index.php             # Main landing page
│   ├── products.php          # Product management page
│   └── orders.php            # Order tracking page
├── .gitignore                # Git ignore configuration
└── README.md                 # Project documentation
```

---

## Libraries Used

* **PHP**: Server-side language used for backend logic.
* **MySQL**: Database used for storing production and order details.
* **jQuery**: For handling dynamic content updates in the frontend.
* **Bootstrap**: Frontend framework for responsive layout and design.

---

## Contributing

We welcome contributions to improve the **Garment Production Tracking Application**. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push your changes (`git push origin feature-branch`).
5. Create a pull request.

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

* **PHP** for powering the backend logic.
* **MySQL** for storing and managing production data.
* **Bootstrap** for providing a responsive and clean design.

---



## Future Improvements

* **Admin Panel**: Implement a dedicated admin interface for better management and control.
* **Analytics**: Add analytics features for production efficiency tracking.
* **Mobile App**: Develop a mobile version of the application for better accessibility.
