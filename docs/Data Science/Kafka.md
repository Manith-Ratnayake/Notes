Kafka Topics 
---------------------

* Topic : A particular stream of data
* Like a table in database
* Can have many topics required 
* A topic is identified by name 
* Any kind of message format (textfile, Binary, JSON) 
* The sequence of messages is called data stream 
* You cannot query topics, kafka producers to send data and kafka consumers to read the data 


Topics are split in partitions 
    - Messages within the partition are orderd
    - Each message within a partition gets an increment id, called offset 
    - 

Topics are immutable, once data is written to a partition, it cannot be changed 
Data is kept for a week (configurable, default 1 week )
Offset have a meaning for a specific partition 
Offset are not reused even if previous message have been deleted 
Order is guaranteed only within a partition (not across partitions)
Data is assigned randomly to a partition unless a key is provided
For a topic can have many partitions 


Producers
--------------------------------------------------

Producers write to topics also knows which partition to use (which kafka broker has it)
Once the data is written to a partition. It cannot be changed (immutability)
Kafka broker failure, producers will automatically recover 
Data is kept only for a limited time 


Producer: Message key
- Producers can choose to send key with the message
- If key = null, data is sent round robin 
- If key != null then all messages for that key will always go to the same partion (hashing) 
- A key are typically sent if you need message ordering for a specific field 



Kafka Message Anatomy 
---------------------------------------------------



Kafka Message Serializer
--------------------------------------------

Kafka only accepts bytes as an input from producers and sends bytes out as an output to consumers. 
Message serialziation means transforming objects / data into bytes 
They are used on the value and key 
Common serilizer := String, Int, Avro, JSON, Protobuf 


Kafka Message Key Hashing 
------------------------------

A kafka partitioner is a code logic that takes a record and determines to which partition to send it 
Key hashing is the process of determining the mapping of a key to partition 

targetPartition = Math.abs(Utils.murmur2(keyBytes)) % (numPartitions - 1)


Consumers
-----------------------------

Consumers read data from  a topic - pull model 
Consumers automatically know which broker to read from 
If borker failure, consumers know how to recover 
Data is read in order from low to high offset (within each partition)


Consumer Deserialzier 
-----------------------------

Deserilizer indicate how to transform bytes into objects 
They are used on the value and the key of the message 
The serialziation / deserialzier type must not change during a topic lifecycle (new topic)


Consumer Groups
---------------------

All the consumers in an application read data as a consumer groups
Each consumer within a group reads from exclusive partitions 
If have more consumers than partitions, some consumers will inactive 
In apache kafka it is acceptable to have multiple consumer groups on the same topic 
But within 1 consumer group only partition can be read by 1 consumer  



Delivery for semantics 
-----------------------------

Default, java consumers will automatically commit offset (at least on)
There are 3 delivery semantics if choose commit manually, 

    - At least once (prefered)
        * offsets are commited after the message is processed 
        * if the processing goes wrong, the message is processed 
        * This can result in duplicate processing of messages, !Make sure processing is idempotent
                (Processing again the messages wont impact your system)

    - At most once 
        * Offsets are commited as soon as messages are recieved 
        * If the processing goes wrong, some messages will be lost (wont be reading again)

    - Exactly One 
        * for kafka -> use the transactional API 
        * for kafka - external system workflow, use an idempotent consumer


Kafka Brokers
---------------------

A kafka cluster is composed of multiple brokers(servers)
Each broker is identified with its ID 
Each broker contains certain topic partitions 
After connecting to any broker (called a bootstrap broker), you will be connected to the entire cluster 
    (Kafka clients have smart mechanics for that)

Data is distributed, broker 1 does not have any Topic B data (not belonging)


Kafka Broker Dicovery
------------------------------

Every kafka broker is also called a bootstrap server 
That means only required to connect to 1 broker and kafka client knows how to connect to entire cluster
Each broker knows about all brokers, topics and partitions (metadata)


Topic Replication Factor 
---------------------------------

Topic should have a replication factor > 1 
This way if a broker is down, another broker can serve the data 

Leader 
---------------

Any time only 1 broker can be a leader for a given partition
Producers can only send data to the broker that is leader of a partition 
The other brokers will replicate the data 
Each partition has one leader and multiple ISR(in sync replica) 


Possible to configure consumers to read from the closet replica (kafka 2.4 + )
This helps in latency, decrease network cost 


Producer Acknowledgement (Acks)
--------------------------------------

ack  = 0 (producer wont wait for ack [possible data loss])
ack  = 1 (producer will wait for leader ack [limited data loss])
acks = all (leader + replicas ack [no data loss])


ZooKeeper
------------------------------

Manages brokers (keeps a list of them)
Helps in performing leader election for partition 
Sends notifications to kafka in case of change 

!!!
Version are not supported
Less secure
In future without ZooKeeper

Kafka Brokers - 
Kafka client - 
 

Kafka KRaft 
---------------------

ZooKeeper shows scaling issues when kafka clusters have > 100,000 partitions 
By removing ZooKeeper, Kafka can scale to 1 million of partitions 

Kafka is now implementing Raft protocol (KRaft) in order to replace ZooKeeper


