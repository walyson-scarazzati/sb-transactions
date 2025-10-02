# Spring Batch Transactions

Project from "Curso Otimização de desempenho para jobs Spring Batch" - Udemy: https://www.udemy.com/course/otimizacao-de-desempenho-para-jobs-spring-batch/

Project to demonstrate how Spring Batch manages transactions within a chunk.
The project has a job that reads a user file and inserts them into the database.

## Roadmap

- [ ] [Transaction control with 1 database](https://github.com/giuliana-bezerra/sb-transactions/tree/v1.0)
- [ ] [Transaction stops working with the addition of a new database for writing](https://github.com/giuliana-bezerra/sb-transactions/tree/v2.0)
- [ ] [Adjust to use transaction in the secondary database](https://github.com/giuliana-bezerra/sb-transactions/tree/v3.0)

## References

- [YouTube Video](https://youtu.be/iZXYG7fM8jI)
- [Spring Batch Course](https://www.udemy.com/course/curso-para-desenvolvimento-de-jobs-com-spring-batch/?referralCode=8743E206FA9240686B20)

## How to Run
1. Ensure you have Java and Maven installed.
2. Place your input files in the `files/` directory.
3. Configure your database and application settings in `src/main/resources/application.properties`.
4. Start required services with Docker Compose:
   ```sh
   docker compose up -d
   ```
   This will start the services defined in `src/main/resources/docker-compose.yml`.
5. Build the project:
   ```sh
   ./mvnw clean package
   ```
6. Run the application:
   ```sh
   java -jar target/transactions-multiples-dbs-<version>.jar
   ```
