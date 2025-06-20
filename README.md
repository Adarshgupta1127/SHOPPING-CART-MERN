🛒Shopping Cart-MERN
Table of Contents
About the Project
Features
Tech Stack
Getting Started
Prerequisites
Installation
Environment Variables
Running the Application
Project Structure
API Endpoints (Optional but Recommended)
Usage
Contributing
License
Contact
Acknowledgements
About The Project
Shopping cart mern is a modern, full-stack e-commerce shopping cart application built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. It provides a seamless and intuitive user experience for Browse products, adding them to a cart, and managing orders.

Features
User Authentication: Secure user registration, login, and logout.
Product Catalog: Browse a list of available products with details.
Shopping Cart Management:
Add/remove items from the cart.
Adjust product quantities in the cart.
View cart summary and total price.
Responsive UI: Designed to work well on various screen sizes (desktop, tablet, mobile).
[Add any other specific features your project has, e.g., product search, filtering, order history, admin panel, payment integration (even if simulated), etc.]
Tech Stack
Frontend:
React.js – Component-based architecture for dynamic user interfaces.
Tailwind CSS – Utility-first CSS framework for rapid and responsive UI development.
shadcn/ui – Beautiful, headless UI components for a polished design.
Framer Motion – Declarative animations and motion effects for engaging user interactions.
React Router – Client-side routing for navigating between different pages.
Axios – Promise-based HTTP client for efficient API communication.
Backend:
Node.js – Server-side JavaScript runtime for building scalable network applications.
Express.js – Fast, unopinionated, minimalist web framework for building robust APIs.
MongoDB – NoSQL document database for flexible and scalable data storage.
Mongoose – Elegant MongoDB object modeling for Node.js, simplifying data interactions.
JWT (JSON Web Token) – Secure and stateless authentication and authorization for user sessions.
Getting Started
Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
Before you begin, ensure you have the following installed:

Node.js & npm:
Download from nodejs.org.
Verify installation:
Bash

node -v
npm -v
Important Note: This project was developed with Node.js 10.14.2. While it might work on newer versions, if you encounter issues, consider using a Node Version Manager (like nvm for macOS/Linux or nvm-windows for Windows) to install and use the specific version:
Bash

nvm install 10.14.2
nvm use 10.14.2
MongoDB:
Local: Install MongoDB Community Server from mongodb.com/try/download/community and ensure it's running.
Cloud (Recommended for ease): Create a free-tier cluster on MongoDB Atlas. You will get a connection URI to use.
Installation
Clone the repository:

Bash

git clone https://github.com/ankitjhagithub21/shopping-cart-mern.git
cd shopping-cart-mern
If you intend to push this to your own GitHub repository, remember to set your remote URL:

Bash

git remote set-url origin https://github.com/Adarshgupta1127/SHOPPING-CART-MERN.git
Install Server Dependencies:

Bash

cd server
npm install
Install Client Dependencies:

Bash

cd ../client
npm install
Environment Variables
Both the server and client directories require .env files to configure environment-specific settings.

Server Configuration (server/.env)
Create a file named .env in the server directory with the following content (replace placeholders with your actual values):

Code snippet

MONGO_URI=[Your MongoDB Connection URI] # e.g., mongodb://localhost:27017/shopping_cart_db OR your Atlas URI
PORT=5000
JWT_SECRET=[A_STRONG_RANDOM_SECRET_KEY_FOR_JWT_AUTHENTICATION]
MONGO_URI:
For local MongoDB, it's typically mongodb://localhost:27017/[your_database_name].
For MongoDB Atlas, copy the connection string provided in your cluster overview.
PORT: The port the backend server will run on. Default is 5000.
JWT_SECRET: A strong, unique string for signing JSON Web Tokens. Generate a complex one!
Client Configuration (client/.env)
Create a file named .env in the client directory with the following content:

Code snippet

VITE_REACT_APP_API_URL=http://localhost:5000/api # Adjust port if your backend runs on a different one
VITE_REACT_APP_API_URL: This should point to the base URL of your backend API. Make sure the port matches your server/.env PORT.
Running the Application
Open two separate terminal windows for the client and server.

Start the Backend Server:

In the first terminal, navigate to the server directory:
Bash

cd shopping-cart-mern/server
Run the server:
Bash

npm start
You should see a message indicating the server is running (e.g., "Server running on port 5000").
Start the Frontend Client:

In the second terminal, navigate to the client directory:
Bash

cd shopping-cart-mern/client
Run the client development server:
Bash

npm run dev
This will typically open the application in your web browser at http://localhost:5173 (or similar port assigned by Vite).
Project Structure
The project is divided into two main directories:

client/: Contains the React.js frontend application.
src/: Main source code for the React app.
components/: Reusable React components.
pages/: Top-level page components.
api/ (or services/): API calls using Axios.
assets/: Images, icons, etc.
server/: Contains the Node.js/Express.js backend API.
models/: Mongoose schemas for MongoDB.
routes/: API routes.
controllers/: Logic for handling API requests.
middleware/: Express middleware (e.g., for authentication).
config/: Database connection setup.
API Endpoints (Optional but Recommended)
Here's a brief overview of some expected API endpoints:

Authentication:

POST /api/auth/register - Register a new user
POST /api/auth/login - Authenticate user and return JWT
GET /api/auth/profile - Get authenticated user's profile (requires JWT)
Products:

GET /api/products - Get all products
GET /api/products/:id - Get a single product by ID
Cart:

GET /api/cart - Get user's cart (requires authentication)
POST /api/cart/add - Add item to cart
PUT /api/cart/update - Update item quantity in cart
DELETE /api/cart/remove - Remove item from cart
Orders:

POST /api/orders - Create a new order (requires authentication)
GET /api/orders - Get user's order history (requires authentication)
Usage
Once both the client and server are running:

Open your browser to http://localhost:5173 (or the port Vite provides).
Register a new user account or log in if you have one.
Browse the product listings.
Add items to your cart, adjust quantities, and proceed to a simulated checkout.
[Describe any other key interactions or flows a user might experience.]
Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

Fork the Project
Create your Feature Branch (git checkout -b feature/AmazingFeature)
Commit your Changes (git commit -m 'Add some AmazingFeature')
Push to the Branch (git push origin feature/AmazingFeature)
Open a Pull Request
