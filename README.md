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

