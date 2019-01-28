---
layout: post
title:  "SageDB: a learned database system"
tags: [database, the-morning-paper, learning, tech]
---

The idea is to build models based on the data stored in the database and how the workload, handled by the database, is distributed.

[Morning paper link](https://blog.acolyer.org/2019/01/16/sagedb-a-learned-database-system/)
[Paper link](http://cidrdb.org/cidr2019/papers/p117-kraska-cidr19.pdf)

Based on these models, better data structures and algorithms used by the database will be built. Thus doing away with generic-one-solutions-fits-all currently implemented with most databases.
* * *

This idea has far reaching implications as it affects the storage of data, how data is accessed, how data is inserted or updated and how query optimisation is done. 
* * *

This idea will basically dynamically tune a database based on the specific use case implemented. Further the tuning is not based on coarse-grained use cases, but rather very specific use cases. This is possible as all the information required to implement specific models is available to the database and thus result in specialised models per database per use case.
* * *

In the past we normally had a single database product (e.g. MS SQL Server or Postgres) with multiple databases serving different applications. Will this idea lead to having different models per database? The assumption is that it would as each database have different, all be it similar, workloads and data stored. Imagine a single database product with multiple accounting databases. Even with similar data being stored (e.g. accounting data), the workload on each database can differ wildly. The volume of data and by extension the query optimisation will differ as well. Applying this idea, implies each database will fundamentally behave different based on a specialised version of the same use case.

* * *

## Why is this interesting?

`This approach, which we call “database synthesis” will allow us to achieve unprecedented performance by specializing the implementation of every database component to the specific database, query workload, and execution environment.`
* * *

Using models, built through neural networks and other methods, can change the runtime behaviour of databases. Assuming here, but it could mean the runtime behaviour of a database can change over time. Which thinking about it is quite an interesting problem to solve. What would happen if the index storage of a database is deemed inefficient and needs be changed based on the models?
* * *

Less developer / DBA database optimisation
* * *

### Further things to understand/learn/read more about

* B-tree
* R-tree
* [RMI model](https://blog.acolyer.org/2018/01/09/the-case-for-learned-index-structures-part-ii/)
* TPC-H benchmark
* TPUs
* Overfitting

* * *
