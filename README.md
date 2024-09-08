# EcommerceCartSyste
## Setup

### Backend Setup

1. *Clone the Repository:*
   bash
   git clone https://github.com/yourusername/CartManagementSystem.git
   cd CartManagementSystem
   

2. *Install Dependencies:*
   bash
   npm install
   

3. *Configure Environment Variables:*
   - Create a .env file in the root directory with necessary variables.

4. *Start the Backend Server:*
   bash
   npm start
   

### Frontend Setup

1. *Navigate to Client Directory:*
   bash
   cd client
   

2. *Install Frontend Dependencies:*
   bash
   npm install
   

3. *Configure Environment Variables:*
   - Create a .env file in the client directory with necessary variables.

4. *Start the Frontend Development Server:*
   bash
   npm run dev
   

## Endpoints + Postman

### API Endpoints

*Product Endpoints*

- *GET /api/products*
  - *Description:* Retrieves all products.
  - *Response:* Array of product objects.

*Cart Endpoints*

- *POST /api/cart*
  - *Description:* Adds or updates a product in the cart.
  - *Request Body:*
    json
    {
      "userId": "exampleUserId",
      "productId": "exampleProductId",
      "quantity": 1
    }
    
  - *Response:* Updated cart object.

- *PUT /api/cart/:id*
  - *Description:* Updates the quantity of a product in the cart.
  - *Request Body:*
    json
    {
      "quantity": 2
    }
    
  - *Response:* Updated cart object.

- *DELETE /api/cart/:id*
  - *Description:* Removes a product from the cart.
  - *Request Body:*
    json
    {
      "productId": "exampleProductId"
    }
    
  - *Response:* Updated cart object.

- *GET /api/cart*
  - *Description:* Fetches the current state of the user's cart.
  - *Query Parameters:*
    - userId: User’s ID.
  - *Response:* Cart object with total price.

### Testing with Postman

1. *Install Postman:*
   - Download and install from [Postman’s website](https://www.postman.com/downloads).

2. *Import API Collection:*
   - Import the provided Postman collection file (if available) or create a new one.

3. *Configure Environment Variables:*
   - Set MONGO_URI, VITE_API_URL, and PORT in Postman’s environment settings.

4. *Test Endpoints:*
   - *GET /api/products*: Send a GET request to retrieve all products.
   - *POST /api/cart*: Send a POST request to add a product to the cart.
   - *PUT /api/cart/:id*: Send a PUT request to update the quantity of a product in the cart.
   - *DELETE /api/cart/:id*: Send a DELETE request to remove a product from the cart.
   - *GET /api/cart*: Send a GET request to retrieve the current state of the user's cart.

Ensure the backend server is active before performing these tests.

---