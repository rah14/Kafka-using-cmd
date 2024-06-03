# 🟡 Apache Kafka Command Line Practice

This repository provides a comprehensive collection of commands for running and practicing Apache Kafka through the command line. It serves as a practical guide for anyone looking to enhance their skills in using Apache Kafka efficiently.

## ⭐ Features

- 📜 Detailed command-line instructions for setting up and managing Apache Kafka
- 📚 Step-by-step guides for various Kafka operations
- 🔄 Examples of common Kafka use cases and scenarios

## 🚀 Getting Started

To get started with practicing Apache Kafka commands, clone this repository and follow the instructions provided in the documentation.

## 📦 Open Source Kafka Startup in Local

1. **Start Zookeeper Server**
    🏃‍♂️
    ```sh
    bin/zookeeper-server-start.sh config/zookeeper.properties
    ```
    Starts the Zookeeper server required for managing Kafka brokers.

2. **Start Kafka Server / Broker**
    🚀
    ```sh
    bin/kafka-server-start.sh config/server.properties
    ```
    Starts the Kafka server to handle message streaming.

3. **Create Topic**
    🛠️
    ```sh
    bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic MyTopic --partitions 3 --replication-factor 1
    ```
    Creates a new topic named `MyTopic` with 3 partitions and a replication factor of 1.

4. **List All Topic Names**
    🔍
    ```sh
    bin/kafka-topics.sh --bootstrap-server localhost:9092 --list
    ```
    Lists all the topics available in the Kafka server.

5. **Describe Topics**
    ℹ️
    ```sh
    bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic MyTopic
    ```
    Provides detailed information about the `MyTopic` topic.

6. **Produce Message**
    📤
    ```sh
    bin/kafka-console-producer.sh --broker-list localhost:9092 --topic MyTopic
    ```
    Opens a console to produce messages to the `MyTopic` topic.

7. **Consume Message**
    📥
    ```sh
    bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic MyTopic --from-beginning
    ```
    Opens a console to consume messages from the `MyTopic` topic from the beginning.

## 📦 Confluent Kafka Community Edition in Local

1. **Start Zookeeper Server**
    🏃‍♂️
    ```sh
    bin/zookeeper-server-start etc/kafka/zookeeper.properties
    ```
    Starts the Zookeeper server for Confluent Kafka.

2. **Start Kafka Server / Broker**
    🚀
    ```sh
    bin/kafka-server-start etc/kafka/server.properties
    ```
    Starts the Kafka server for Confluent Kafka.

3. **Create Topic**
    🛠️
    ```sh
    bin/kafka-topics --bootstrap-server localhost:9092 --create --topic MyTopic1 --partitions 3 --replication-factor 1
    ```
    Creates a new topic named `MyTopic1` with 3 partitions and a replication factor of 1 in Confluent Kafka.

4. **List All Topic Names**
    🔍
    ```sh
    bin/kafka-topics --bootstrap-server localhost:9092 --list
    ```
    Lists all the topics available in the Confluent Kafka server.

5. **Describe Topics**
    ℹ️
    ```sh
    bin/kafka-topics --bootstrap-server localhost:9092 --describe --topic MyTopic1
    ```
    Provides detailed information about the `MyTopic1` topic in Confluent Kafka.

6. **Produce Message**
    📤
    ```sh
    bin/kafka-console-producer --broker-list localhost:9092 --topic Topic1
    ```
    Opens a console to produce messages to the `MyTopic1` topic in Confluent Kafka.

7. **Consume Message**
    📥
    ```sh
    bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic MyTopic1 --from-beginning
    ```
    Opens a console to consume messages from the `MyTopic1` topic from the beginning in Confluent Kafka.

8. **Send CSV File Data to Kafka**
    📥
    ```sh
    bin/kafka-console-producer --broker-list localhost:9092 --topic MyTopic1 < bin/data.csv
    ```
    Sends data from a CSV file to the `MyTopic1` topic in Confluent Kafka.

---

Feel free to adjust any specific details to better match the content and focus of this repository. I hope this guide helps you get up and running with Apache Kafka. Happy learning! 🎉
