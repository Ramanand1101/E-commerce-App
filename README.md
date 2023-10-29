# Funky Online Store API

Funky Online Store API is a backend service for an e-commerce application that handles user authentication, product management, cart management, order placement, and address management. It provides various endpoints to support these functionalities.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/funky-online-store-api.git
   ```

2. Install dependencies:

   ```bash
   cd funky-online-store-api
   npm install
   ```

3. Set up your environment variables. Create a `.env` file in the root directory and add the necessary environment variables as shown in the [Environment Variables](#environment-variables) section.

4. Start the server:

   ```bash
   npm start
   ```

Deployed link [https://celadon-basbousa-d43b06.netlify.app/](https://celadon-basbousa-d43b06.netlify.app/).

## Usage

The API provides various endpoints for user registration, login, product management, cart management, order placement, and address management. You can make requests to these endpoints using tools like [Postman](https://www.postman.com/) or any HTTP client library.

## Endpoints

### User Routes

- **POST /api/user/register:** Register a new user.
- **POST /api/user/login:** Login with an existing user account.
- **GET /api/user/getnewtoken:** Get a new access token using a refresh token.
- **POST /api/user/logout:** Logout and blacklist the refresh token.

### Product Routes

- **GET /api/products:** Get products with optional search, sort, and filter parameters.
- **POST /api/products/search:** Search products by name or description.
- **POST /api/products/create:** Create a new product.
- **PATCH /api/products/update/:id:** Update product details by ID.
- **DELETE /api/products/delete/:id:** Delete a product by ID.

### Cart Routes

- **GET /api/cart:** Get items in the cart for the authenticated user.
- **POST /api/cart/add:** Add a product to the cart.
- **PUT /api/cart/update/:id:** Update the quantity of an item in the cart.
- **DELETE /api/cart/remove/:id:** Remove an item from the cart.

### Order Routes

- **POST /api/orders/placed:** Place a new order.
- **GET /api/orders:** Get all orders.
- **GET /api/orders/:orderId:** Get a specific order by ID.
- **PUT /api/orders/:orderId/complete:** Update order status to complete.
- **DELETE /api/orders/order/delete/:orderId/:itemId:** Delete an item from an order.

### Address Routes

- **POST /api/address:** Add a new shipping address to an existing order.

## Environment Variables

- **PORT:** Port number for the API server (default: 3000)
- **MONGO_URL:** MongoDB connection URL
- **SECRET_KEY:** Secret key for generating JWT tokens
- **REFRESH_SECRET_KEY:** Secret key for generating refresh tokens
- **GOOGLE_CLIENT_ID:** Google OAuth client ID
- **GOOGLE_CLIENT_SECRET:** Google OAuth client secret
- **GOOGLE_CALLBACK_URL:** Google OAuth callback URL
Deploy link: https://celadon-basbousa-d43b06.netlify.app/
Example .env file:

```plaintext
PORT=3000
MONGO_URL="mongodb+srv://username:password@cluster0.mongodb.net/database"
SECRET_KEY="your-secret-key"
REFRESH_SECRET_KEY="your-refresh-secret-key"
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
GOOGLE_CALLBACK_URL="http://localhost:3000/oauth/auth/google/callback"
```

**Note:** Ensure that you replace the placeholder values with your actual credentials.

## Contributing

Contributions are welcome! If you find any issues or want to add new features, feel free to open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).









