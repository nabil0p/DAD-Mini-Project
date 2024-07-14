# Custom PC Shop Project

This project involves multiple applications to manage a custom PC shop, including user authentication, product management, and purchasing functionalities.

## Applications Involved

### 1. User Authentication Service
- **Description**: Manages user registration and login.
- **Endpoints**:
  - `POST /register`: Register a new user.
  - `POST /login`: Login an existing user.

### 2. Product Management Service
- **Description**: Handles the product inventory, including listing, updating, and searching products.
- **Endpoints**:
  - `GET /products`: Retrieve a list of all products.
  - `GET /products/{id}`: Retrieve details of a specific product by ID.
  - `PUT /products/{id}`: Update the details of a specific product by ID.
  - `POST /products/search`: Search for products based on criteria.
  - `GET /products/search`: Search for products based on criteria (alternative method).

## Architecture/Layer Diagram

### User Authentication Service


### Product Management Service


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

### User Authentication Service
- **Database**: `auth_db`
- **Tables**:
  - `users`: Stores user information such as email, password, and name.

### Product Management Service
- **Database**: `product_db`
- **Tables**:
  - `products`: Stores product details including ID, title, price, product code, description, quantity, and status.

## Database Schema

### `users` Table
| Column    | Type    | Description                  |
|-----------|---------|------------------------------|
| id        | INT     | Primary Key                  |
| email     | VARCHAR | User's email address         |
| password  | VARCHAR | User's hashed password       |
| name      | VARCHAR | User's name                  |
| created_at| TIMESTAMP| Record creation timestamp   |
| updated_at| TIMESTAMP| Record update timestamp     |

### `products` Table
| Column        | Type      | Description                    |
|---------------|-----------|--------------------------------|
| id            | INT       | Primary Key                    |
| title         | VARCHAR   | Product title                  |
| price         | DOUBLE    | Product price                  |
| product_code  | VARCHAR   | Unique code for the product    |
| description   | TEXT      | Product description            |
| quantity      | INT       | Available quantity             |
| status        | VARCHAR   | Product status (e.g., active)  |
| created_at    | TIMESTAMP | Record creation timestamp      |
| updated_at    | TIMESTAMP | Record update timestamp        |

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
    - Create `auth_db` and `product_db` databases.
    - Run the provided SQL scripts to create the tables.

4. **Run the User Authentication Service**:
    ```sh
    cd auth-service
    ./run.sh
    ```

5. **Run the Product Management Service**:
    ```sh
    cd product-service
    ./run.sh
    ```

6. **Access the application**:
    - User Authentication: `http://localhost:8000`
    - Product Management: `http://localhost:8000/products`

Enjoy managing your Custom PC Shop!
