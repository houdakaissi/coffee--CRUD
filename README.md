# Coffee CRUD Application - Backend

This is the backend of the Coffee CRUD Application, developed using Bun with TypeScript. It handles the CRUD operations for coffee entries and connects to a PostgreSQL database via Prisma.

## Features

- Handle API requests for creating, reading, updating, and deleting coffee entries.
- Direct communication with the database using ZenStack and Zod for type-safe data retrieval and validation.
- Containerized PostgreSQL database with Docker.

## Setup Instructions

### Prerequisites

- **Bun** (for the backend runtime environment)
- **Docker** (for PostgreSQL container)
- **Node.js** (for development purposes if you need to run things outside Bun)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/coffee-crud-backend.git
   cd coffee-crud-backend
