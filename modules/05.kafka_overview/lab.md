# Quick Kafka Demo

Complete the [Kafka quick start guide](https://kafka.apache.org/quickstart) through step 5. Note that you will need complete step one to download and untar kafka on your local machine to be able to access the cli commands. For step two, choose the `Using GraalVM Based Native Apache Kafka Docker Image` option. Finally, in order to stop the kafka environment complete step eight along with  stopping the docker container.   

**BONUS**

Adapt the wikimedia streaming demo in the wikimedia_get_raw_stream_data notebook from the packaging module and write a quick connector to read data from the wiki stream into a Kafka topic. **Note** You may want to use either the [kafka-python](https://pypi.org/project/kafka-python/) library or the [confluent-kafka](https://pypi.org/project/confluent-kafka/) library. As an additional note, the confluent-kafka library may be the better choice as it is more actively maintained ( there was a nearly 5 year gap on commits to the other project and in general it is a good practice to choose the more well maintained dependency. )
