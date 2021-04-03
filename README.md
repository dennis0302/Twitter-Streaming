# Real-time streaming data pipeline for Twitter

This is a data pipeline to stream live tweets through Kafka and storing tweets in Elasticsearch (Bonsai, managed Elasticsearch).


# Usage

1. Start Zookeeper and Kafka in Terminal


```
zookeeper-server-start.sh config/zookeeper.properties

kafka-server-start.sh config/server.properties
```


2. Twitter API configuration

```
Create a twitter account if you do not already have one.
Go to https://developer.twitter.com/ and log in with your twitter credentials.
Go to Developer Portals and Click "Create New App"
Fill out the forms and agree to the terms
Generate and copy API key & secret and Access token & secret
```

Fill keys and tokens TwitterProducer.java

```
String consumerKey = "";
String consumerSecret = "";
String token = "";
String secret = "";
```


3. Bonsai - Managed Elasticsearch setup

```
Create a free account if you do not already have one.
Click Credentials to get full access URL
Copy the entire URL 
```

Fill hostname, username and password TwitterConsumer.java from the URL

```
String hostname = "";
String username = "";
String password = "";
```

4. Write terms that you want to stream from Twitter in TwitterProducer.java

```
// Example
List<String> terms = Lists.newArrayList("sports", "soccer", "basketball");
```

5. Run TwitterProducer.java and TwitterConsumer.java
