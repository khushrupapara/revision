# Database Queries

## Quick Overview

| Name           | Definition                                              | Example                    |
| -------------- | ------------------------------------------------------- | -------------------------- |
| Database Query | A request used to read or change data in a database.    | Get all users from a table |
| SQL            | A language commonly used to communicate with databases. | `SELECT * FROM users;`     |
| Database       | A system that stores and organizes data.                | User records and orders    |
| Table          | A structure that stores data in rows and columns.       | `users` table              |

## 1. Database Query

**Definition:** A database query is a request to read, add, update, or delete data in a database.

**Example:**

```sql
SELECT name, email
FROM users
WHERE age > 18;
```

**Instructions:**

* Use queries to retrieve or modify structured data.
* Use conditions such as `WHERE` to get only the required records.
* Always validate queries before changing or deleting data.
* Give agents only the database permissions they actually need.

## 2. SQL

**Definition:** SQL (Structured Query Language) is a language commonly used to interact with relational databases.

**Example:**

```sql
-- Read data
SELECT * FROM users;

-- Add data
INSERT INTO users (name, email)
VALUES ('Alice', 'alice@example.com');

-- Update data
UPDATE users
SET email = 'new@example.com'
WHERE name = 'Alice';

-- Delete data
DELETE FROM users
WHERE name = 'Alice';
```

**Instructions:**

* `SELECT` reads data.
* `INSERT` adds new data.
* `UPDATE` changes existing data.
* `DELETE` removes data, so use it carefully.

## 3. AI Agent + Database

**Definition:** An AI agent can use database tools to retrieve or modify stored information while completing a task.

**Example:**

```text
User
  ↓
AI Agent
  ↓
Creates Database Query
  ↓
Database
  ↓
Returns Data
  ↓
AI Agent
  ↓
Final Answer
```

**Instructions:**

* Use database queries when the answer depends on current stored data.
* Let the agent generate queries based on the user's request.
* Restrict database access with appropriate permissions.
* Validate AI-generated queries, especially queries that modify or delete data.

## Quick Memory

```text
Database Query → Request to read or change data
SQL → Language used to communicate with databases
SELECT → Read data
INSERT → Add data
UPDATE → Change data
DELETE → Remove data
```
