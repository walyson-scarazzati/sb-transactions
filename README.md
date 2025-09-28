# Spring Batch Transactions

Projeto para demonstrar como o Spring Batch gerencia transações dentro de um chunk.
O projeto possui um job que lê um arquivo de usuários e os insere no banco de dados.

## Roteiro

- [ ] [Controle transacional com 1 banco de dados](https://github.com/giuliana-bezerra/sb-transactions/tree/v1.0)
- [ ] [Transação deixa de funcionar com a adição de um novo banco para escrita](https://github.com/giuliana-bezerra/sb-transactions/tree/v2.0)
- [ ] [Ajustar para utilizar transação no banco secundário](https://github.com/giuliana-bezerra/sb-transactions/tree/v3.0)

## Referências

- [Vídeo do Youtube](https://youtu.be/iZXYG7fM8jI)
- [Curso de Spring Batch](https://www.udemy.com/course/curso-para-desenvolvimento-de-jobs-com-spring-batch/?referralCode=8743E206FA9240686B20)

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