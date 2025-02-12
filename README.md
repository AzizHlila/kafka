## 🚀 Quick Start

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/AzizHlila/kafka.git
cd kafka
```

### 2️⃣ Start Kafka and Zookeeper
```
docker-compose up -d
```
## 🎯 Usage (Test)
### 1️⃣ Create a Kafka Topic
```
docker exec -it kafka kafka-topics --create --topic test-topic --bootstrap-server localhost:29092 --partitions 1 --replication-factor 1
```
### 2️⃣ List Topics
```
docker exec -it kafka kafka-topics --list --bootstrap-server localhost:29092
```
### 3️⃣ Start a Kafka Producer
```
docker exec -it kafka kafka-console-producer --broker-list localhost:29092 --topic test-topic
```
### 4️⃣ Start a Kafka Consumer
```
docker exec -it kafka kafka-console-consumer --bootstrap-server localhost:29092 --topic test-topic --from-beginning
```
