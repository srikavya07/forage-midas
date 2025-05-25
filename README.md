Forage Midas Core Project

This repository contains my completed solution for the JPMorgan Chase Midas Core virtual experience hosted on Forage. The project simulates a real-world core banking system that processes transactions using event-driven architecture.

🚀 Project Overview

The goal of this project is to implement a backend system that:

Processes user transactions using Apache Kafka

Interacts with an external Incentive API

Stores user data and transaction history using an H2 in-memory database

Exposes a REST API to retrieve user balances

🔧 Technologies Used

Java 17

Spring Boot

Apache Kafka

H2 Database

Spring Data JPA

REST API (via Spring Web)

✅ Features Implemented

Transaction Listener: Listens to a Kafka topic for new transaction messages.

Validation & Persistence: Validates incoming transactions and stores valid ones.

Incentive API Integration: Sends transaction data to an external service and applies returned incentive amount to the recipient's balance.

User Balance Endpoint: Exposes a GET /balance?userId=X endpoint that returns the user's balance.

Custom Port: The application runs on port 33400.

📁 Project Structure
├── src/main/java/com/jpmc/midascore
│   ├── component         # Business logic (TransactionHandler, DatabaseConduit)
│   ├── controller        # REST controllers (BalanceController)
│   ├── entity            # Entity classes (UserRecord, etc.)
│   ├── foundation        # Domain models (Transaction, Incentive, Balance)
│   └── MidasCoreApplication.java
├── src/test/java        # Task test classes (TaskOneTests, TaskFiveTests, etc.)
├── services             # External Incentive API JAR (runs on port 8080)
└── application.properties

▶️ Running the Project
1. Start the Incentive API JAR:
cd services
java -jar incentives-api.jar

2.Run the main Spring Boot application:
./mvnw spring-boot:run

3.Access the balance endpoint:
GET http://localhost:33400/balance?userId=5
