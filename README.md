Create Single Kafka through docker using the file docker-compose.single.yml by running the below command

**docker-compose -f docker-compose.single.yml up -d**

Similarly, create kafka cluster through docker using the file docker-compose.cluster.yml by running the below command

**docker-compose -f docker-compose.cluster.yml up -d**

Notes:

Keywords

Topic: a channel for data streaming between producers and consumers
Offset: identity of last message consumed by consumer
Partitions: one topic can be divided into multiple partitions can be shared to consumers of same group
Key: any unique identifier to identify your message
Message: any unique identifier to identify your message
Multiple instance of same service must have same consumer group id, whereas different services must have different consumer group id to receive messages.
Partition rebalancing happens automatically, whenever consumer join and leave. For example, if a topic was created with four partitions, two consumer with same consumer group id consuming the messages. In that case, two partitions will be assigned to one consumer instance and two partitions will be assigned to the other consumer. When one consumer left, rebalancing event will take place. Then, all four partition will be assigned to one consumer. When new consumer join the group, rebalancing will occur again.
