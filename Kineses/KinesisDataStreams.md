# Kinesis Data Stream 
You can use Amazon Kinesis Data Streams to collect and process large streams of data records in real time. You can create data-processing applications, known as Kinesis Data Streams applications. A typical Kinesis Data Streams application reads data from a data stream as data records. These applications can use the Kinesis Client Library, and they can run on Amazon EC2 instances.


## Kinesis Data Streams High-Level Architecture
The following diagram illustrates the high-level architecture of Kinesis Data Stream:
1. The producers continually push data to Kinesis Data Streams.
2. The consumers process the data in real time.
3. Consumers (such as a custom application running on Amazon EC2 or Amazon Kinesis Data firehose delivery stream) can store thier results using:
    - Amazon dynamodb
    - Amazon redshift
    - Amazon S3

![alt](./assets/architecture.png)

## Kinesis Data Streams Terminology


### Kinesis Data Stream
A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by kinesis data streams.

### Data Record
A data record is the unit of data stored in a Kinesis data stream. DAta records are composed of a sequence number, a partition key and a data blob, which is an immutable sequence of bytes. Kinesis Data Streams does not inspect, interpret, or change the data in the blob in any way. A data blob can be up to 1 MB.


### Capacity Mode
A data stream capacity mode determines how capacity is managed and how you are charged for the usage of your data stream.
- On-demand monde
> Kinesis Data Streams automatically manages the shards in order to provide the necessary throughput. You are charged only for the actual throughput that you use and Kinesis Data Streams automatically accommodates your workloads’ throughput needs as they ramp up or down. 
- Provisioned mode
> you must specify the number of shards for the data stream. The total capacity of a data stream is the sum of the capacities of its shards. You can increase or decrease the number of shards in a data stream as needed and you are charged for the number of shards at an hourly rate.

### Retention Period
The retention period is the length of time that data records are accessible after they are added to the stream. A stream’s retention period is set to a default of 24 hours after creation. You can increase the retention period up to 8760 hours.

### Producer
Producers put records into Amazon Kinesis Data Streams. For example, a web server sending log data to a stream is a producer.

### Consumer
Consumers get records from Amazon Kinesis Data Streams and process them. 

### Shard
- Streams are divided into shards
- A shard has a sequence of data records in a stream
- it serves as a base throughput unit of a kinesis data stream
- A shard supports 1 MB/Second and 1,000 records per second for writes and 2 MB/second for reads.

### Partition Key
- A partition key is used to group data by shard within a stream. Kinesis Data Streams segregates the data records belonging to a stream into multiple shards.
- It uses the partition key that is associated with each data record to determine which shard a given data record belongs to.
- Partition keys are Unicode strings, with a maximum length limit of 256 characters for each key.
- An MD5 hash function is used to map partition keys to 128-bit integer values and to map associated data records to shards using the hash key ranges of the shards. 
- When an application puts data into a stream, it must specify a partition key.


### Sequence Number
- Each data record has a sequence number that is unique per partition-key within its shard.
- Kinesis Data Streams assigns the sequence number after you write to the stream with client.putRecords or client.putRecord.
- Sequence numbers for the same partition key generally increase over time.
- The longer the time period between write requests, the larger the sequence numbers become.


### Kinesis Client Library
- The Kinesis Client Library is compiled into your application to enable fault-tolerant consumption of data from the stream.
- The Kinesis Client Library ensures that for every shard there is a record processor running and processing that shard. 

