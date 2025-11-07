# Wikimedia EventStreams Processing

[link for docs](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams_HTTP_Service)

## TODO

- explore the incoming wikimedia change events. Note that in the "source" stream we can change some other parameters. For instance, the stream that will be connected only monitors change events to fr.wikipedia. Refer to the documentation and tune the stream to provide information that is of interest to you, like monitoring the page of your favorite athlete, author, topic, etc.
- build at least one new schema in the unity catalog to aggregate events for later analysis. This can be as simple as the "bronze" level of data processing (creating a database of essentially the raw events with minor cleaning/only information that is of interest) to the "gold" level of data processing (data ready for consumption by downstream partners, specific for dashboards, etc)
- Look through the data and imagine that there is an event that there is an event you want to react to. For this exercise, find an event that happens rarely, but has happened at least once for the period that has been monitored. You will simulate an alerting system by creating a new schema/volume to send these monitored events to once they have happened. 
- write a simple job that can be scheduled to clear out the raw data being loaded into the "source" and schedule it to run via the databricks ui. Note that you will want to schedule this for a short window for testing purposes and once confirmed working correctly schedule it to run at longer intervals like once daily.
- once you have the clean up job set and data processing code, you can create a small pipeline that schedules the stream to run periodically, coordinate the processing job to run after and finally the clean up job once you have ensured that you dont accidentally remove unprocessed data.
