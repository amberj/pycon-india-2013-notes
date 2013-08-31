## Graph Everything
### [Kunal Kerkar](twitter.com/tsudot)

#### Outline
1. Data at Plivo
2. Graphite
3. Carbon Daemons
4. Congiuring Carbon
5. Whisper Database
6. Render URL API

#### Components
* OpenSIPS
* Django
* PostgreSQL
* Redis
* Sbinken
* Tank
* HomR (?)
* ??
* ??

#### What we wanted 
* Track calls/sms
* Number of recharges, signups
* etc.

#### Graphite
* Open source.
* Stores numeric time series data and it renders graphs of this data on demand.

#### Graphite architecture in nutshell
* carbon: a Twisted daemon that listend for time-series data
* whisper: 
* graphite webapp:

#### Carbon Daemons
* 1 daemon, `carbon-cache.py`
	* Accepts  metrics
	* Writes them to disk
	* `carbon.conf`
	* `storage-schemas.conf`
* Listen for time-series data on few protocols (zeroMQ, pickle, plaintext etc.)
* `carbon-relay.py`
	* Helps in achieving
		* replication
		* sharding
	* Relay methods
		* ??
		* ??

#### Protocols
* Plaintext protocol
* pickle protocol 

#### Whisper
* Fixed size database
* Fast, reliable storage of data
* Long term retention

#### Whisper
* Aggregation
	* Collapse multiple data points
	* Uses `avg` by default (can be setup)
* Efficiency

#### Graphite at Plivo
* `pip install graphite-web`

#### Other stuff (summary)
* Render URL API
* Graphene

#### Q&A
Q: Real time data analysis in Graphite?
> A: Graphene allows it(?)

Q: What is fixed size DB?
> A: Define the size in advance.

Q: Plivo v/s Asterisk?
> A: Plivo is better, in his opinion. It scales very well. 

Q: Which graph format?
> A: Graphite does SVG. Graphene does graphs in JS.

Q: What is retention period?
> A: We show data everyday. Every month they aggregate this data.
