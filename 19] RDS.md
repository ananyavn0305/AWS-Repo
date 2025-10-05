## Easy Questions
1. What is Amazon RDS?  
   - Managed relational database service in AWS.

2. Name some RDS engines supported by AWS.  
   - MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Aurora.

3. What is the main purpose of a database?  
   - To store, retrieve, and manage data efficiently.

4. What does DBMS stand for?  
   - Database Management System.

5. What is a relational database?  
   - Database that stores data in tables with rows and columns.

6. What is a non-relational database?  
   - Database that stores data without tables, rows, or foreign keys.

7. What is a primary key?  
   - A unique identifier for each record in a table.

8. What is a foreign key?  
   - A column that links to the primary key of another table.

9. What is the difference between RDS and a self-managed database?  
   - RDS is fully managed, self-managed requires manual setup and maintenance.

10. What is Amazon Aurora?  
    - AWS cloud-native relational database compatible with MySQL/PostgreSQL.

## Moderate Questions

1. What are the advantages of using RDS?  
   - Automated backups, patching, scaling, and high availability.

2. How do you connect an EC2 instance to an RDS database?  
   - Allow inbound DB port traffic in security group, then connect using the endpoint.

3. Which ports are used by MySQL and PostgreSQL?  
   - MySQL: 3306, PostgreSQL: 5432.

4. What is the maximum size of an RDS database?  
   - Depends on engine; e.g., Aurora: up to 128 TB.

5. Explain automated backups in RDS.  
   - RDS automatically backs up database daily and allows point-in-time recovery.

6. What is Multi-AZ deployment in RDS?  
   - High availability setup with synchronous replication to a standby in another AZ.

7. Can you scale RDS vertically and horizontally?  
   - Yes; vertical: larger instance, horizontal: read replicas.

8. What is a read replica in RDS?  
   - Replica database to offload read traffic and improve performance.

9. How do you secure an RDS instance?  
   - Using security groups, encryption at rest (KMS), and SSL connections.

10. How do you restore an RDS database from a snapshot?  
    - Use snapshot to launch a new RDS instance.

## Hard Questions
1. Explain the difference between Single-AZ and Multi-AZ RDS deployments.  
   - Single-AZ: one instance; Multi-AZ: primary + standby in another AZ for failover.

2. What is RDS Proxy and why is it used?  
   - Managed database proxy that improves application scalability and resiliency.

3. How does RDS handle failover in Multi-AZ deployment?  
   - Automatically switches to standby in case of primary instance failure.

4. Can you explain the differences between Aurora MySQL and standard MySQL on RDS?  
   - Aurora offers better performance, storage auto-scaling, and cloud-native replication.

5. How does RDS handle backups and snapshots differently?  
   - Backups are automated and continuous; snapshots are user-initiated and manual.

6. How would you optimize RDS performance for high read traffic?  
   - Use read replicas, caching (ElastiCache), and proper indexing.

7. What is the difference between synchronous and asynchronous replication in RDS?  
   - Synchronous ensures data is replicated before commit; asynchronous replicates after commit.

8. Can RDS be integrated with CloudWatch? If yes, for what?  
   - Yes; for monitoring metrics, performance, and setting alarms.

9. How do you migrate an on-premises database to Amazon RDS?  
   - Using AWS Database Migration Service (DMS) or snapshot import.

10. What is point-in-time recovery (PITR) in RDS?  
    - Restores database to any specific time using automated backups and transaction logs.

## Scenario-Based

1. Your RDS MySQL instance crashes unexpectedly. How would you restore service quickly?  
   - Launch a new RDS instance from the latest automated backup or snapshot.

2. You have heavy read traffic on your database affecting performance. What would you do?  
   - Create read replicas to offload read traffic from the primary instance.

3. You need high availability across multiple AZs. How will you configure RDS?  
   - Enable Multi-AZ deployment for automatic failover.

4. You want to migrate a production on-premises PostgreSQL database to AWS without downtime. How?  
   - Use AWS Database Migration Service (DMS) with ongoing replication.

5. Your database contains sensitive data. How will you secure it in RDS?  
   - Enable encryption at rest using KMS and enforce SSL connections.

6. A developer accidentally deleted a table in RDS. How can you recover it?  
   - Restore the database to a point-in-time before the deletion.

7. Your Aurora instance needs to scale storage automatically. How do you achieve this?  
   - Aurora automatically scales storage up to 128 TB based on usage.

8. You want to monitor CPU, memory, and storage of your RDS instance. How?  
   - Enable CloudWatch monitoring and set alarms for metrics.

9. You need to reduce failover time during Multi-AZ switchover. What would you do?  
   - Use RDS Proxy to maintain persistent connections and reduce downtime.

10. A client requests a database that can handle bursts of read/write with minimal latency. Which RDS engine do you recommend?  
    - Amazon Aurora, due to its cloud-native design and high throughput.
