# SQL Lite3 101
Personal notebook on how to use SQL Lite 3

## When to Use SQLite

1. **Embedded Applications**:
   - **Mobile Applications**: SQLite is commonly used in mobile apps (iOS, Android) for local data storage.
   - **Desktop Applications**: Suitable for lightweight desktop applications that need a simple database solution without the overhead of a client-server database system.

2. **Development and Testing**:
   - **Prototyping**: Great for developing and testing applications quickly due to its simplicity and ease of setup.
   - **Local Development**: Ideal for local development environments where a full-fledged database server is unnecessary.

3. **Small to Medium-Sized Websites**:
   - **Content Management Systems**: Suitable for small to medium-sized websites where the database size and concurrent access are limited.

4. **IoT Devices**:
   - **Embedded Systems**: Useful for Internet of Things (IoT) devices where a lightweight database is needed for storing configuration data or sensor readings.

5. **Single-User Applications**:
   - **Personal Projects**: Perfect for personal projects and applications that don't require multi-user access or complex transactions.

6. **Read-Heavy Applications**:
   - **Static Content**: Applications that perform a lot of read operations with fewer writes, such as reference materials, catalogs, or documentation systems.

## When Not to Use SQLite

1. **High-Concurrency Applications**:
   - **Web Applications with High Traffic**: Not suitable for high-concurrency environments where many users access and modify the database simultaneously. SQLite handles multiple readers well but struggles with many concurrent writers.

2. **Large Databases**:
   - **Big Data Applications**: SQLite is not designed to handle very large databases (hundreds of gigabytes or more) efficiently. A more robust RDBMS like PostgreSQL, MySQL, or Microsoft SQL Server would be better for such cases.

3. **Complex Transactions**:
   - **Enterprise Applications**: Applications requiring complex transaction management, extensive reporting, and advanced database features are better served by a full-fledged RDBMS.

4. **Distributed Databases**:
   - **Multi-Node Clusters**: If your application requires distributed database support with replication and sharding, SQLite is not suitable. Use databases like PostgreSQL, MySQL, or NoSQL databases like Cassandra.

5. **Security Requirements**:
   - **Highly Sensitive Data**: While SQLite can be encrypted, it lacks the advanced security features of other RDBMSs, making it less suitable for applications with stringent security requirements.

6. **Scalability Requirements**:
   - **Growing Applications**: If you anticipate your application to grow significantly in terms of data volume and user base, you may outgrow SQLite's capabilities. Planning for scalability from the start with a more robust RDBMS might be better.

## Summary

**Use SQLite When**:
- You need a simple, lightweight, and self-contained database.
- You are developing small to medium-sized applications.
- The application has low to moderate concurrency requirements.
- You need an embedded database for mobile or IoT devices.
- You are prototyping or developing locally.

**Avoid SQLite When**:
- The application requires high concurrency with many simultaneous writers.
- You need to manage very large databases.
- Complex transaction management and advanced database features are needed.
- The application requires distributed database support.
- High security and scalability are primary concerns.