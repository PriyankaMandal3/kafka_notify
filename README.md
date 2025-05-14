# Real-Time Notification System using Kafka and Go

This project is a real-time notification system built using **Go**, **Apache Kafka**, **Docker**, and **Gin Web Framework**. It allows producers to send notifications to a Kafka topic and consumers to retrieve and process those notifications.

## Features

- RESTful API to send notifications via Kafka (Producer)
- Real-time Kafka consumer that processes incoming notifications
- Dockerized services for easy deployment
- Built using Go, Gin, and Sarama Kafka client
- Tested with Postman for API interactions

---

## Technologies Used

- [Go](https://golang.org/)
- [Gin Web Framework](https://github.com/gin-gonic/gin)
- [Sarama Kafka Client](https://github.com/Shopify/sarama)
- [Apache Kafka](https://kafka.apache.org/)
- [Docker](https://www.docker.com/)
- [Postman](https://www.postman.com/)

---

## System Architecture
+-----------+ +-------------------+ +---------------------+
| Postman | ----> | Gin Producer API | ---> | Kafka 'notifications' Topic |
+-----------+ +-------------------+ +---------------------+
|
v
+------------------------+
| Kafka Consumer Service |
+------------------------+


---

## Getting Started

### Prerequisites

- Docker & Docker Compose
- Go 1.18+
- Postman (for API testing)

---



---

## 🚀 Getting Started

Follow these steps to run the complete project on your machine.

---

### Step 1: Start Kafka & Zookeeper
docker-compose up -d

### Step 2: Start the Producer
### Step 3: Start the Consumer
### Step 4: Sending Notifications



