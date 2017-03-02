# Elasticsearch (implemented using Python)

## Installation
    1. Download elasticsearch from [https://www.elastic.co/downloads/elasticsearch](https://www.elastic.co/downloads/elasticsearch)
    2. Make sure your java is updated. Also, double check which java version is compatible with the version of elasticsearch you just downloaded. Refer to [https://www.elastic.co/support/matrix#show_jvm](https://www.elastic.co/support/matrix#show_jvm)
    ```terminal
    java -version
    ```
    3. Download elasticsearch python module by entering the following command into your terminal:
    ```terminal
    sudo pip install elasticsearch
    ```

## Get Started
```
$ cd ~/elasticsearch-5.x.x
$ ./bin/elasticsearch
```

## Terminology
__near real time (NRT)__: Slight delay or latency between time of indexing data and when it is available for searches.
__cluster__: A collection of one or more servers (or nodes). The default name of __cluster__ is Elastic Search.
__node__: A single single server.
__index__: A collection of similar documents. E.g. an __index__ for all customer data.
__type__: A logical category or partition.
__document__: A basic unit of information that can be indexed. __Documents__ are usually expressed in javascript notation which is light weight. E.g. a document for a product, a document for a customer, etc.
__shard__: An index can potentially store a large amount of data which can sometimes exceed our hardware limits. Elasticsearch provides the ability to subdivide our index into multiple pieces. The subdivision of our index is called shard. When we create an index, we can simply define the number of shards we want. __Shards__ are also known as a Lucene index. Contains segments (mini-indexes). In some cases, shards are used to distribute data across one index. You cannot split a shard.
__replica__: Copy/backup of an index. 
__segment__: Inside each __segment__, there are a data structures such as inverted index, stored fields, document values, etc. __Segments__ are immutable. 
__field cache__: In a document value data structure, if you don't specify that you want these documents values, Elasticsearch will use what's called a __field cache__. A __field cache__ will load all the values for the field in the entire index into memory. This is quite fast to use, but will use tons of memory.


## Notes
### Deleting Documents
When deleting a document, there's a bitmap that marks the document as deleted. And Lucene will filter it out for every subsequent search but the segment itself doesn't change. So in an update, for example, is essentially our delete followed by a reindex so.

### Sharding & Partitioning
An elasticsearch index with two shards searching one elasticsearch index with two shards is essentially the same as searching two elastic search indexes with one shard each. In both cases you are searching across two shards that is two leucine indexes. Sharding and partition into different indexes are two different yet similar approaches to slicing up your data to prepare for handling data massive amounts.

### Log Partition
Partitioning data by one index, per day. This is extremely useful if you only need data by day or only current data.


### Think Long Term (sharding)
You cannot split shards. You can, however, easily add more nodes and move shards around. 

### Why Sharding is Important
Shards allows for two important features:
1. Horizontally scalable
2. Allows us to distribute and parallelize operations across shards



