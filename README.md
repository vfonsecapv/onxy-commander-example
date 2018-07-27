# onyx-commander-example

We read commands from a Kafka topic, process them with Onyx, and produce materialized views using Datomic.
Commands generate read-receipts named events, which are fed back into Kafka to provide a point of synchronicity
for the initial caller of a command.

### Usage

- Spin up ZooKeeper and Kafka with Docker compose: `docker-compose up`
- Open the test under `onyx-commander-example/test/onyx_commander_example/jobs/commander_test.clj`
- If your Docker IP isn't `127.0.0.1`, change the ZooKeeper and Kafka hosts at the top of the file
- Run the test with `lein test`
