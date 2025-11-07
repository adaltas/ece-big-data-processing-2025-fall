---
Duration: 3 houres
---

# Application packaging and submitting

## Spark functionalities recap

- Batch processing with:
  - Resilient Distributed Datasets
  - Resilient Distributed DataFrames
- Structured Streaming processing

And also:

- Spark MLlib:
  - Distributed model training
  - Apply models to data
- GraphX: distributed graph processing

## Spark application components

- Java and Scala: "Uber" **jar** file
  - Spark code
  - Dependencies (libraries)
- Python: .py, .zip or .egg files

## Spark application configuration

- Deploy mode: client or cluster
- Driver and executors:
  - Memory
  - Cores
  - Number of executors

## Spark application monitoring

- One web UI per application
- Track:
  - Jobs
  - Stages
  - Executors

## Spark application performance tuning

- Limit number of shuffles
- 3 partitions / CPU
- Start big, then reduce memory
- Lot of testing, monitoring, benchmarking (optimize properties one by one)

---

*The content of this document, including all text, images, and associated materials, is the exclusive property of Adaltas and is protected by applicable copyright laws. Unauthorized distribution, reproduction, or sharing of this content, in whole or in part, is strictly prohibited without the express written consent of the author(s). Any violation of this restriction may result in legal action and the imposition of penalties as prescribed by law.*
