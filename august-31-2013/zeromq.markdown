## Build your next Python project - Super fast, distributed and infinitely scalable, using ZeroMQ
## [Srinivasan R](https://twitter.com/cnu)

#### Queues
* Require message brokers. Central point of failure
    * For e.g. Apache ActiveMQ, RabbitMQ, StormMQ, Redis

#### ZeroMQ
* No message broker. 
* Almost zero latency.
* Similar to AMQP
* No dependency on server HAVING to be up.
    * Handles any order of socket binding
* Lots of transport protocol
    * tcp
    * inproc
    * ipc
    * pgm,epgm
        * Smart multicast protocol
* Available for lots of languages
* No supervision systems available, nothing to fallback on


#### ZeroMQ: Basic Patterns
* Request/Reply
* Publish/Subscribe
* Pipelining
* Paired sockers
    * Can do distributed tasks
    * User uploads 100 images to album, 10 servers running in parallel = faster
    * Server = Ventilator
    * Client = Worker
    * End point = Sink
    * Ventilator need to wait for the workers to join else tasks are all taken up by the first fellow.

##### Resources
* [zero.mq](http://zeromq.org/community)
* [zguide.zeromq.org](http://zguide.zeromq.org/page:all)
* [github.com/cnu/zeromq-talk](https://github.com/cnu/zeromq-talk)