# 🚕 Cab Booking App - Kafka-Based Microservices Architecture

This project demonstrates a simplified **Cab Booking Application** built using **Apache Kafka** to handle asynchronous communication between microservices. The app mimics real-world scenarios like booking a cab, driver assignment, and trip status updates using Kafka topics.

---

## 🛠️ Tech Stack

- **Apache Kafka** – Event streaming platform for inter-service communication
- **Spring Boot** – For building RESTful microservices
- **Kafka Streams / Kafka Consumer/Producer APIs** – For stream processing and event handling
- **Zookeeper** – Kafka dependency for broker coordination

---

## 🧩 Architecture Overview

```text
[User] ---> [Booking Service] ---> [Kafka Topic: booking-requests]
                                     |
                                     v
                            [Driver Service Consumer]
                                     |
                          [Kafka Topic: driver-responses]
                                     |
                                     v
                            [Trip Management Service]
