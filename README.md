# Custom PC Shop Project

This project involves multiple applications to manage a custom PC shop, including user authentication, product management, and purchasing functionalities.

## Applications Involved

### 1. Web Administrator (Laravel)
- **Description**: This web application is used by administrators to manage users and products. It is built using the Laravel framework.


### 2. Customer Application (Java Swing)
- **Description**: This desktop application allows customers to login and purchase products. It is built using Java Swing.


## Architecture/Layer Diagram

### Web Administrator (Laravel)


### Customer Application (Java Swing)



### Middleware


## List of URL Endpoints (Middleware RESTful)

### User Authentication Endpoints
- `POST /register`: Register a new user.
- `POST /login`: Login an existing user.

### Product Management Endpoints
- `GET /products`: Retrieve a list of all products.
- `PUT /products/{id}`: Update the details of a specific product by ID.

## Functions/Features in the Middleware

- **Authentication Middleware**: Verifies the user's credentials during login.
- **Authorization Middleware**: Ensures the user has the necessary permissions to perform certain actions.
- **Logging Middleware**: Logs all the incoming requests and outgoing responses for monitoring and debugging purposes.

## Database and Tables Involved

### User Authentication and Product Management (Laravel Database)
![Database Schema](path/to/database/schema/image.png)

### `users` Table
| Column             | Type            | Description                      |
|--------------------|-----------------|----------------------------------|
| id                 | bigint unsigned | Primary Key                      |
| name               | varchar(255)    | User's name                      |
| email              | varchar(255)    | User's email address             |
| email_verified_at  | timestamp       | Email verification timestamp     |
| password           | varchar(255)    | User's hashed password           |
| level              | varchar(255)    | User's level/role                |
| remember_token     | varchar(100)    | Token for "remember me" feature  |
| created_at         | timestamp       | Record creation timestamp        |
| updated_at         | timestamp       | Record update timestamp          |

### `products` Table
| Column        | Type            | Description                    |
|---------------|-----------------|--------------------------------|
| id            | bigint unsigned | Primary Key                    |
| title         | varchar(255)    | Product title                  |
| price         | varchar(255)    | Product price                  |
| product_code  | varchar(255)    | Unique code for the product    |
| description   | varchar(255)    | Product description            |
| quantity      | varchar(255)    | Available quantity             |
| status        | varchar(255)    | Product status (e.g., active)  |
| created_at    | timestamp       | Record creation timestamp      |
| updated_at    | timestamp       | Record update timestamp        |

## How to Run the Project

1. **Clone the repository**:
    ```sh
    git clone https://github.com/your-repo/custom-pc-shop.git
    ```

2. **Navigate to the project directory**:
    ```sh
    cd custom-pc-shop
    ```

3. **Set up the databases**:
    - Create `laravel_db` database.
    - Run the provided SQL scripts to create the tables.

4. **Run the Laravel Web Administrator**:
    ```sh
    cd web-administrator
    php artisan serve --host 192.168.1.116
    ```

5. **Run the Customer Application (Java Swing) in Eclipse**:
    - Open Eclipse IDE.
    - Import the Java project:
      - Go to `File > Import`.
      - Select `Existing Projects into Workspace` under the `General` category.
      - Click `Next`.
      - Browse to the directory where your Java project is located.
      - Select the project and click `Finish`.
    - Run the `LoginForm` class:
      - In the `Package Explorer`, navigate to the `LoginForm` class.
      - Right-click on `LoginForm` and select `Run As > Java Application`.

6. **Access the application**:
    - Web Administrator: Open your web browser and go to `http://192.168.1.116:8000`.
    - Customer Application: Run the Java Swing application from Eclipse as described above.

