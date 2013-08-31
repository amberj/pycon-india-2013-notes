## Logging on Steroids - How we manage logs at Inmobi
### Ajay Yadav

#### Logs
* Server logs (gunicorn, nginx etc.)
* Regexes!
	* Example: Looong, cryptic email matching regex
	* You need Regex ninjas
	* Hard to remember
	* Hard to reproduce
	* Hard to test
	* Tedious to search in distributed systems

#### Better solution: Structured Logging
* For e.g. Windows event logs (recent versions use XML)
* Easy indexing, faster searching, scales well
* Various formats: thrift, json, csv, protobuf, xml etc.
* JSON is what Inmobi uses.
	* Why JSON? Lighweight. Widely supported in programming languages. Not tied to any particular framework
	* Python/Django: python-json-logger.

#### Logstash
* Open source, easy, scalable.
* Can be used with other libraries (modular design).
* Easily extendable.
* Supports both standalone mode as well as full fledged setup.

#### Input
<code>
input {
	file {
		type => "nginxlog"
		path => ("/var/log/nginx/")
		format => json
	}
}
</code>

#### Filters
* Apply patterns and extract data
* Tag your stream of logs (ditinguish between DB, app, server logs etc)
* ~30 ready to use filters.

<code>
filter {
	grok {
		type => "postfix"
		pattern => ["%{SYSLOGBAS}"]
		add_tag => ["postfix", "email"]
	}
}
</code>

* grok
	* recommended way to parse patterns testable, repeatable
	* Easy to add your own patterns
	* Comes with over 100 patterns
	* Caters to common needs like logs from nginx, postgresql etc

#### Patterns
* Match and extract specific data

#### grok-patterns
<code>
%{syntax:semantic}
</code>
<code>
%{POSINT:PID:int}</code>
* Supports int, float etc.

#### Output
* Over 50 output formats supported.
* For e.g. Message queue, graphite, zeromq, rabbitMQ etc.

#### Sample output
TBD
<code></code>

#### Querying/Analytics UI
* Graylog2
* Graphite
* Kibana (Default logstash UI)

#### Graylog2
* Used by Inmobi
* Support for Python/Django (graypy from PyPI)
* Accepts messages over TCP, UDP...
* Allows stream level access

#### Alternatives
* **Transport**:
	* Inmobi's conduit (open source project)
	* **Search/Analytics**: Hadoop, graylog2, elsa
	* **Storage**: hdfs, cassandra, elastic search
	* **More**: loggly, logster, apache-falcon, lumberjack

#### Q&A

Q: How much is increase of size of storing structured logs?
> A: Logstash does compression before storing in Elastic Search. For most needs, a couple nodes are sufficient.

Q: Performance for searching the logs? How to ensure that
> A: Works well for logs coming from thousands of users. Several hundred of GBs in a second or two. It depends on how good you are indexing. You can use Elastic Search clusters etc for scalability.

Q: How do you generate analytics for these logs? At Inmobi? For some custom events?
> A: Response code, response time, alerts. No need to write loads of code (just write simple config files). You have to specify custom events.

Q: If certain events happening, how to check DB, server, health logs etc?
> A: You can customize your analytics dashboard. 

Q: Logs for clicks etc?
> A: Beacon ping analysis, Hadoop, Conduit
