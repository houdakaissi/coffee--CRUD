Coffee CRUD Application - Backend
This is the backend of the Coffee CRUD Application, developed using Bun with TypeScript. It handles the CRUD operations for coffee entries and connects to a PostgreSQL database via Prisma.

Features
Handle API requests for creating, reading, updating, and deleting coffee entries.
Direct communication with the database using ZenStack and Zod for type-safe data retrieval and validation.
Containerized PostgreSQL database with Docker.
Setup Instructions
Prerequisites
Bun (for the backend runtime environment)
Docker (for PostgreSQL container)
Node.js (for development purposes if you need to run things outside Bun)
Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/coffee-crud-backend.git
cd coffee-crud-backend
Install dependencies using Bun:

bash
Copy
Edit
bun install
Configure your environment variables in the .env file:

Set the PostgreSQL connection URL for the Prisma client:
plaintext
Copy
Edit
DATABASE_URL="postgresql://user:password@localhost:5432/coffee_db"
Set up and run the PostgreSQL database using Docker:

bash
Copy
Edit
docker-compose up
Apply Prisma migrations to set up the database schema:

bash
Copy
Edit
bun prisma migrate dev
Run the backend:

bash
Copy
Edit
bun run dev
The server should now be running at http://localhost:3001.

Folder Structure
bash
Copy
Edit
/src
  /controllers    # Contains the logic for CRUD operations
  /models         # Coffee model definition using Prisma
  /routes         # Define routes for CRUD operations
  /services       # Business logic layer
  /utils          # Helper functions, middleware, and other utilities
  /validators     # Zod validation for data integrity
/.env             # Environment variables (e.g., database connection)
docker-compose.yml # Docker configuration for PostgreSQL
Docker Integration
To containerize the PostgreSQL database, a docker-compose.yml file is included. It defines the PostgreSQL container and its connection settings.

Run the following command to start the PostgreSQL container:

bash
Copy
Edit
docker-compose up
The PostgreSQL container will be accessible on localhost:5432.

Deployment
This backend application can be deployed using any cloud provider, such as Heroku, AWS, or DigitalOcean.

For example, to deploy on Heroku:

Install the Heroku CLI if you haven’t already.

Login to Heroku:

bash
Copy
Edit
heroku login
Create a Heroku application:

bash
Copy
Edit
heroku create coffee-crud-backend
Push the backend code to Heroku:

bash
Copy
Edit
git push heroku master
Set up PostgreSQL in Heroku:

bash
Copy
Edit
heroku addons:create heroku-postgresql:hobby-dev
Apply Prisma migrations:

bash
Copy
Edit
heroku run "bun prisma migrate deploy"
The live backend will be accessible at the Heroku URL.

Technologies Used
Bun (Runtime)
TypeScript (Static typing)
Prisma (Database ORM)
PostgreSQL (Database)
ZenStack & Zod (Type-safe data handling)
Docker (Containerization for PostgreSQL)
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/my-feature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/my-feature).
Create a pull request.
