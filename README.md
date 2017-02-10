# BigData Fun
I wanted to learn more about big data, and some of the key tools in the market.

As a result, I decided to create an all in one docker environment, including distributed filesystem (HDFS).

The key components are:

- [HDFS](http://hortonworks.com/apache/hdfs) - Distributed file system, including two data nodes
- [HBase](http://hortonworks.com/apache/hbase) - Non-relational, distributed database similar to Google BigTable
- [Hue](http://gethue.com) - Web interface for analyzing data

The following components will be coming soon:

- [Solr](http://lucene.apache.org/solr/) - Search platform based on Lucene
- [Spark](http://spark.apache.org/) - Data processing engine

## Getting started
Oh the joy, it's so easy.

`docker-compose up`

Give it a minute to get its ducks in line, and then access the key things you'll be interested in:

- Hue UI: [http://127.0.0.1:8888](http://127.0.0.1:8888)
- HDFS NameNode UI: [http://127.0.0.1:50070](http://127.0.0.1:50070)
- Thrift UI: [http://127.0.0.1:9095](http://127.0.0.1:9095)
- HBase Master UI: [http://127.0.0.1:16010](http://127.0.0.1:16010)
- HBase Region UI: [http://127.0.0.1:16030](http://127.0.0.1:16030)

## Hue
When you first use Hue, it does a health check and will tell you that a bunch of stuff isn't configured correctly, that's fine as I don't plan to build the whole Cloudera stack, just 'next next next' thought it and use the components that matter, like the [HBase Browser](http://127.0.0.1:8888/hbase/#hbase).

## Credit
The HDFS work has been tackled beautifully by [https://github.com/big-data-europe/docker-hadoop](https://github.com/big-data-europe/docker-hadoop), so I'm using it for namenode, and datanodes.

## TODO
- Solr
- Spark
- Migrate namenode, datanode and hue to my own build on centos base, like HBase.