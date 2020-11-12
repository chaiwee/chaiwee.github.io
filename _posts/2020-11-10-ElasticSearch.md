---
layout: post
title: ElasticSearch
---

1. Introduction
2. What does it do?
3. How does it work?

1. Introduction
People might think that elasticsearch is either an index, a search engine, an analytics database, a big data solution or it's kind of like Google.
The truth is all of the above. Over the years, ElasticSearch and the ecosystem of components that has grown around it called the "Elastic Stack",
has been used for a growing number of use cases, from a simple search on a website or doc, collecting and analyzing log data, to a business intelligence too
for data analysis and visualization. At its core, you can think of Elasticsearch as a server that can process JSON requests and give you back JSON data.

2. What does it do?
- store
- search
- analyze huge volumes of data quickly and in near real-time and give back answers in ms
- achieve fast search responses because instead of searching the text directly, it searches in index
- uses a structure based on documents instead of tables and schemas


3. How does it work?
To understand how it works, let's cover some basic concepts:
- Document
  The basic unit of information that can be indexed in Elasticsearch expressed in JSON, its like a row in a relational DB schema.
  It has a unique ID and a given data type.
  Eg. a document can represent an encyclopedia article or log entries from a web server.
  
- Indices
  An index is a collection of documents that have similar characteristics.
  It is the highest level entity that can be query in elasticsearch, like a database in relational DB schema.
  Elasticseach stores data as JSON documents. Each one correlates a set of keys with their values.
  ES uses a data structure called inverted index, which allows very fast full-text searches.
  An inverted index lists every unique word in any document, then identify all the documents each word occurs in.
  https://www.knowi.com/wp-content/uploads/2020/03/inverse-index-1024x512.webp
  During the indexing process, ES stores documents and builds an inverted index to make the document data searchable in near real-time.
  
- Cluster
  It is a group of one or more node instances that are connected together.
  It distribute tasks, searching and indexing, across all the nodes in the cluster.
  
- Node
  It is a single server that is a part of a cluster.
  It stores data and participate in cluster's indexing and searching capabilities
  a) Master Node
  b) Data Node
  c) Client Node

The Elastic Stack(ELK)
- Logstash: used to aggregate and process data and send it to ES
- Kibana: a data visualization and management tool for ES that provides realtime histogram, line graph, pie chart, and maps.


Elasticsearch supports a variety of languages and official clients are available for:
- Java
- JavaScript (Node.js)
- Go
- .NET (C#)
- PHP
- Perl
- Python
- Ruby

Elastic tutorial coming soon!
