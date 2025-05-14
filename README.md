Here’s your updated and polished `README.md` file, formatted professionally for GitHub:

---

```markdown
# 📬 Real-Time Notification System using Kafka and Go

This project is a real-time notification system built using **Go**, **Apache Kafka**, **Docker**, and the **Gin Web Framework**. It enables a producer to send notifications to a Kafka topic, and a consumer to retrieve and process them.

---

## ✅ Features

- RESTful API to send notifications (Producer)
- Kafka consumer to receive real-time messages
- Dockerized Kafka and Zookeeper services
- Built using Go, Gin, and Sarama
- API tested with Postman

---

## 🛠️ Technologies Used

- [Go](https://golang.org/)
- [Gin Web Framework](https://github.com/gin-gonic/gin)
- [Sarama Kafka Client](https://github.com/Shopify/sarama)
- [Apache Kafka](https://kafka.apache.org/)
- [Docker](https://www.docker.com/)
- [Postman](https://www.postman.com/)

---

## 🧱 System Architecture

```

+-----------+       +-------------------+       +---------------------+
\| Postman   | ----> | Gin Producer API  | --->  | Kafka 'notifications' Topic |
+-----------+       +-------------------+       +---------------------+
|
v
+------------------------+
\| Kafka Consumer Service |
+------------------------+

````

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Go 1.18 or higher
- Docker & Docker Compose
- Postman (for API testing)

---

### 🐳 Step 1: Start Kafka and Zookeeper

Start Kafka and Zookeeper using Docker:

```bash
docker-compose up -d
````

---

### ⚙️ Step 2: Start the Producer API

In one terminal:

```bash
cd cmd/producer
go run producer.go
```

The producer will run on:

```
http://localhost:8080
```

---

### 🔄 Step 3: Start the Kafka Consumer

In another terminal:

```bash
cd cmd/consumer
go run consumer.go
```

The consumer will run on:

```
http://localhost:8081
```

---

### 📫 Step 4: Send Notifications Using Postman

**1. POST Notification**

* **Method:** POST

* **URL:** `http://localhost:8080/send`

* **Body Type:** `x-www-form-urlencoded`

* **Body Parameters:**

  ```
  fromID=1
  toID=1
  message=Hello, this is a test notification!
  ```

* **Expected Response:**

  ```json
  {
    "status": "notification sent successfully"
  }
  ```

---

**2. GET Notifications**

* **Method:** GET

* **URL:** `http://localhost:8081/notifications/1`

* **Expected Response:**

  ```json
  {
    "notifications": [
      {
        "fromID": "1",
        "message": "Hello, this is a test notification!"
      }
    ]
  }
  ```

---

## ✅ Result

Once both services are running and messages are sent via Postman:

* The **Producer API** will confirm message delivery.
* The **Consumer API** will retrieve and display notifications for the user.

---

## 🎉 Successfully Done!

You now have a functioning real-time Kafka-based notification system using Go and Docker!

---

## 📄 License

This project is licensed under the MIT License.

```

---

Let me know if you’d like me to generate a sample Postman collection or `docker-compose.yml` to complete your setup.
```
