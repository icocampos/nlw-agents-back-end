# NLW Agents

This project was developed during Rocketseat's **Next Level Week (NLW)** event, focusing on building a modern, robust, and efficient API using cutting-edge technologies.

## 🚀 Technologies Used

- **Node.js** with native **TypeScript** (`--experimental-strip-types`)
- **Fastify** – High-performance web framework
- **PostgreSQL** with **pgvector** extension for vector support
- **Drizzle ORM** – Type-safe ORM for database operations
- **Zod** – Schema validation with static typing
- **Docker** – Containerized database
- **Biome** – Code linting and formatting

## 🏗️ Architecture

The project follows a clean and modular architecture:

- Clear separation between routes, schemas, and database logic
- Schema validation with **Zod** for type safety
- Type-safe database operations with **Drizzle**
- Centralized environment variable validation

## ⚙️ Setup and Configuration

### Prerequisites

- Node.js (with support for `--experimental-strip-types`)
- Docker and Docker Compose

### Steps

1. Clone the repository:

```bash
git clone <repo-url>
cd server
```

2. Start the database with Docker:

```bash
docker-compose up -d
```

3. Create a `.env` file in the root folder with the following content:

```
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

4. Install the dependencies:

```bash
npm install
```

5. Run the database migrations:

```bash
npx drizzle-kit migrate
```

6. (Optional) Seed the database with sample data:

```bash
npm run db:seed
```

7. Start the project:

**Development mode:**

```bash
npm run dev
```

**Production mode:**

```bash
npm start
```

## 📚 Available Scripts

- `npm run dev` – Runs the server in development mode with hot reload
- `npm start` – Runs the server in production mode
- `npm run db:seed` – Seeds the database with sample data

## 🌐 Available Endpoints

The API will be running at: [http://localhost:3333](http://localhost:3333)