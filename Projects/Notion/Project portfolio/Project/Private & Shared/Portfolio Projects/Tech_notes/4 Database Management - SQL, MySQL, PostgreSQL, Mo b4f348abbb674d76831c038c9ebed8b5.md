# 4. Database Management - SQL, MySQL, PostgreSQL, MongoDB

# Database Management

> Master data storage, retrieval, and management systems
> 

## 📊 Core Concepts

### SQL (Structured Query Language)

**What is SQL?**

SQL is the standard language for managing and manipulating relational databases.

**Key Concepts:**

- DDL (CREATE, ALTER, DROP)
- DML (SELECT, INSERT, UPDATE, DELETE)
- Joins (INNER, LEFT, RIGHT, FULL)
- Aggregation functions (COUNT, SUM, AVG)
- Subqueries and views
- Indexes and optimization
- Transactions and ACID properties
- Normalization (1NF, 2NF, 3NF)

**Learning Resources:**

- 🔗 [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- 🔗 [SQLZoo Interactive Tutorial](https://sqlzoo.net/)
- 🔗 [Mode SQL Tutorial](https://mode.com/sql-tutorial/)
- 🔗 [SQL Bolt Exercises](https://sqlbolt.com/)

**YouTube Tutorials:**

- 🎥 [SQL Full Course - freeCodeCamp](https://www.youtube.com/watch?v=HXV3zeQKqGY)
- 🎥 [SQL Tutorial for Beginners - Programming with Mosh](https://www.youtube.com/watch?v=7S_tz1z_5bA)
- 🎥 [SQL Crash Course - Traversy Media](https://www.youtube.com/watch?v=p3qvj9hO_Bo)

---

### MySQL

**What is MySQL?**

MySQL is the world's most popular open-source relational database management system.

**Key Features:**

- High performance and reliability
- ACID compliance
- Stored procedures and triggers
- Replication and clustering
- Full-text search
- Support for multiple storage engines

**Learning Resources:**

- 🔗 [W3Schools MySQL Tutorial](https://www.w3schools.com/mysql/)
- 🔗 [MySQL Official Documentation](https://dev.mysql.com/doc/)
- 🔗 [MySQL Tutorial](https://www.mysqltutorial.org/)

**YouTube Tutorials:**

- 🎥 [MySQL Database Full Course - freeCodeCamp](https://www.youtube.com/watch?v=ER8oKX5myE0)
- 🎥 [MySQL Tutorial - Programming with Mosh](https://www.youtube.com/watch?v=7S_tz1z_5bA)
- 🎥 [MySQL Crash Course - Traversy Media](https://www.youtube.com/watch?v=9ylj9NR0Lcg)

---

### PostgreSQL

**What is PostgreSQL?**

PostgreSQL is a powerful, open-source object-relational database system known for its robustness and advanced features.

**Key Features:**

- ACID compliant
- Support for JSON and JSONB
- Advanced indexing (GiST, GIN)
- Full-text search
- Window functions
- Common Table Expressions (CTEs)
- Foreign data wrappers

**Learning Resources:**

- 🔗 [W3Schools PostgreSQL Tutorial](https://www.w3schools.com/postgresql/)
- 🔗 [Official PostgreSQL Documentation](https://www.postgresql.org/docs/)
- 🔗 [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)

**YouTube Tutorials:**

- 🎥 [PostgreSQL Tutorial for Beginners - freeCodeCamp](https://www.youtube.com/watch?v=qw--VYLpxG4)
- 🎥 [Learn PostgreSQL - Amigoscode](https://www.youtube.com/watch?v=5hzZtqCNQKk)
- 🎥 [PostgreSQL Crash Course - Traversy Media](https://www.youtube.com/watch?v=qw--VYLpxG4)

---

### MongoDB

**What is MongoDB?**

MongoDB is a popular NoSQL document database that stores data in flexible, JSON-like documents.

**Key Concepts:**

- Documents and collections
- BSON data format
- CRUD operations
- Aggregation framework
- Indexing strategies
- Replication and sharding
- Schema design patterns
- Mongoose ODM (for Node.js)

**Learning Resources:**

- 🔗 [W3Schools MongoDB Tutorial](https://www.w3schools.com/mongodb/)
- 🔗 [Official MongoDB Documentation](https://www.mongodb.com/docs/)
- 🔗 [MongoDB University (Free Courses)](https://learn.mongodb.com/)

**YouTube Tutorials:**

- 🎥 [MongoDB Full Course - freeCodeCamp](https://www.youtube.com/watch?v=c2M-rlkkT5o)
- 🎥 [MongoDB Crash Course - Traversy Media](https://www.youtube.com/watch?v=-56x56UppqQ)
- 🎥 [MongoDB Tutorial - Web Dev Simplified](https://www.youtube.com/watch?v=ofme2o29ngU)

---

## 🔧 Additional Database Technologies

### Redis

**What is Redis?**

Redis is an in-memory data structure store used as a database, cache, and message broker.

**Learning Resources:**

- 🔗 [Redis Official Documentation](https://redis.io/docs/)
- 🔗 [Redis Tutorial](https://www.tutorialspoint.com/redis/)

**YouTube Tutorials:**

- 🎥 [Redis Crash Course - Traversy Media](https://www.youtube.com/watch?v=jgpVdJB2sKQ)
- 🎥 [Redis Tutorial - freeCodeCamp](https://www.youtube.com/watch?v=XCsS_NVAa1g)

### SQLite

**Learning Resources:**

- 🔗 [SQLite Tutorial](https://www.sqlitetutorial.net/)
- 🔗 [W3Schools SQLite](https://www.w3schools.com/sql/sql_ref_sqlite.asp)

**YouTube Tutorials:**

- 🎥 [SQLite Databases - Tech With Tim](https://www.youtube.com/watch?v=byHcYRpMgI4)

### Cassandra

**Learning Resources:**

- 🔗 [Apache Cassandra Documentation](https://cassandra.apache.org/doc/latest/)

**YouTube Tutorials:**

- 🎥 [Cassandra Tutorial - freeCodeCamp](https://www.youtube.com/watch?v=J-cSy5MeMOA)

---

## 📊 SQL vs NoSQL Comparison

| Feature | SQL (Relational) | NoSQL (Non-Relational) |
| --- | --- | --- |
| Data Model | Tables with rows | Documents, Key-Value, Graph |
| Schema | Fixed schema | Flexible schema |
| Scalability | Vertical | Horizontal |
| Transactions | ACID compliant | Eventually consistent |
| Best For | Complex queries, relationships | Large-scale data, flexibility |
| Examples | MySQL, PostgreSQL | MongoDB, Cassandra, Redis |

---

## 🔍 Database Design Best Practices

1. **Normalization** - Reduce data redundancy
2. **Indexing** - Improve query performance
3. **Backup Strategy** - Regular backups and recovery plan
4. **Security** - Access control, encryption
5. **Optimization** - Query optimization, proper indexing
6. **Monitoring** - Track performance metrics

---

## 📝 Practice Projects

1. **Library Management System** - Books, members, loans
2. **E-commerce Database** - Products, customers, orders
3. **Social Network Schema** - Users, posts, friendships
4. **Inventory Management** - Products, suppliers, transactions
5. **Analytics Dashboard** - Data aggregation and reporting