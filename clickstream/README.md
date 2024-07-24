# Clickstream
The **Clickstream** service will collect user events and store the raw data on the 
```Apache Hadoop``` cluster, and **internal consumers** can access the cluster via
```Apache Spark```, ```Presto``` etc. to read processed data in order to use
it in their business logic.

# Architecture
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/images/clickstream-design-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="docs/images/clickstream-design-light.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="docs/clickstream-design-dark.png">
</picture>

# Purpose of Service
We are collecting user events for the reasons listed below:

1. Recommend better **product** or **content** to users based on their 
historical behaviour.
2. Creating **advertising campaigns** based on users' behaviour.
3. Understand how **different page layouts** or **contents** affect users'
behaviour.

# Used Technologies

| Tecnology             | Version | Purpose                                                                                 |
| --------------------- | ------- | --------------------------------------------------------------------------------------- |
| ```Apache Spark```    |  x      | It performs **Extract-Transform-Load** ***(ETL)*** job.                                 |
| ```Apache Kafka```    |  x      | It collects **validated event data** from the service and stores in specific topics.    |
| ```Apache Hadoop```   |  x      | It stores **validated user event data** and **processed data**.                         |
| ```Apache Hive```     |  x      | It stores **metadata** of **validated user event data**.                                |
