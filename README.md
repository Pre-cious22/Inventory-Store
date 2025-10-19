<H1>Inventory/Store Api</H1>

A full RESTful API for store and inventory management built with Node.js, Express, and MongoDB. This API provides complete CRUD operations for managing products, suppliers, and orders, supporting real-world inventory workflows such as stock tracking, order creation, and supplier coordination.
<hr style="border: 2px solid black;">
<h1>Features</h1>

<ul>
  <li>Product Management — Create, read, update, and delete products with fields like SKU, name, price, and stock level.</li>
  <li>Supplier Management — Maintain supplier records with contact information for reordering and inventory sourcing.</li>
  <li>Order Management — Create and manage purchase orders containing multiple items, quantities, and total pricing.</li>
</ul>

<hr>
<h1>Tech Stack</h1>

<ul>
  <li>Runtime: Node.js</li>
  <li>Framework: Express.js</li>
  <li>Database: MongoDB (using Mongoose ODM)</li>
  <li>Database Hosting: MongoDB Atlas</li>
  <li>Additional Libraries: dotenv, cors, morgan, nodemon</li>
</ul>
<hr>
<h1>Installation</h1>

Step 1: Clone or Download the Project
# If using Git
git clone <your-repository-url>
cd inventory-api

Step 2: Install Dependencies
npm install

<h3>Step 3: Set Up MongoDB Atlas</h3>
<h2>1. Create a MongoDB Atlas Account<h2/>
  
<ul>
  <li>Go to MongoDB Atlas </li>
  <li>Sign up for a free account</li>
</ul>

<h3>2. Create a New Cluster</h3>
<ul>
  <li>Click “Build a Database”</li>
  <li>Choose “M0 FREE” tier</li>
  <li>Select a cloud provider and region (nearest to you)</li>
  <li>Click “Create”</li>
</ul>

<h3>3. Create a Database User</h3>
<ul>
  <li>Go to Database Access (left sidebar)</li>
  <li>Click “Add New Database User”</li>
  <li>Username: inventoryAdmin (or your choice)</li>
  <li>Password: generate a strong one — SAVE THIS!</li>
  <li>User Privileges: Atlas admin</li>
  <li>Click “Add User”</li>
</ul>

<h3>4. Configure Network Access</h3>
<ul>
  <li>Go to Network Access (left sidebar)</li>
  <li>Click “Add IP Address”</li>
  <li>Select “Allow Access from Anywhere (0.0.0.0/0)”</li>
  <li>Click “Confirm”</li>
</ul>

<h3>5. Get Connection String</h3>
<ul>
  <li>Go to Database (left sidebar)</li>
  <li>Click “Connect” on your cluster</li>
  <li>Choose “Connect your application”</li>
  <li>Copy the connection string</li>
</ul>

<h3>Step 4: Configure Environment Variables</h3>
Create a .env file in the project root:

PORT=5000
MONGO_URI=mongodb+srv://inventoryAdmin:YOUR_PASSWORD@cluster0.xxxxx.mongodb.net/inventory-api?retryWrites=true&w=majority
NODE_ENV=development

Important:
<ul>
  <li>Replace YOUR_PASSWORD with your MongoDB password</li>
  <li>Replace the cluster URL with your actual connection string</li>
  <li>Add /inventory-api before the ? to specify the database name</li>
</ul>

<hr>
<h3>Step 5: Seed the Database</h3>
Populate your MongoDB with sample data:

npm run seed

You should see something like:
MongoDB Connected: cluster0-xxxxx.mongodb.net
✅ Data seeded successfully!
   - 3 products created
   - 4 suppliers created
   - 3 orders created
<hr>
<h1>How to Run</h1>
<h2>Development Mode (with auto-restart):</h2>
npm run dev

You should see:

Server running in development mode on port 5000
MongoDB Connected: cluster0-xxxxx.mongodb.net
✅ Your API is now running at: http://localhost:5000


