AMQP
=====

Library for accessing RabbitMQ from Haskell. Please see the [Hackage docs](http://hackage.haskell.org/packages/archive/amqp/latest/doc/html/Network-AMQP.html) for an example.

Changelog
=========

### Version 0.10.0

* the maximum number of channels can now be set

### Version 0.9.0

* add 'global' flag for qos

### Version 0.8.3

* implement closeChannel

### Version 0.8.0

* TLS support
* new helper function rejectEnv
* new field exchangeArguments in ExchangeOpts
* new module Network.AMQP.Lifted with consumeMsgs functions lifted to MonadBaseControl

### Version 0.7.0

* new function fromURI to parse AMQP URIs
* heartbeat support

### Version 0.6.0

* new function addReturnListener which allows specifying a handler for returned messages
* new function openConnection'' with support for most AMQP connection options
* better error message on failed connection handshake

### Version 0.5.0

* support for AMQP 0-9-1
* new function consumeMsgs' which allows you to pass in a field-table
* new function bindExchange allows for binding an exchange to another exchange
* new function unbindQueue allows unbinding a queue from an exchange
* new function unbindExchange allows unbinding an exchange from an exchange

### Version 0.4.3

* use Handles instead of sockets 
* fix deprecation warnings from Data.Binary

### Version 0.4.2

* add (Read, Ord, Eq, Show) instances for most data-types

### Version 0.4.1

* add queueHeaders field to QueueOpts

### Version 0.4

* Data.Text is now used instead of Strings. Using the _OverloadedStrings_ extension will make upgrading easier
* the field-types in Network.AMQP.Types should now be more compatible with RabbitMQ
* hostnames passed to openConnection will now be resolved
* basic QoS support
* exceptions thrown in a callback will not erroneously close the channel anymore