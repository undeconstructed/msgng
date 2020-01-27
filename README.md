# msgng

An idea about internet scale messaging. Maybe there could be a sort of email style system, intended to allow automation and control by ordinary people.

Persistent-ish, store and forward messaging allows sending messages to a person, i.e. an identifier that would normally be owned by an individual. Such messages would make their way to a "pod", owned and controlled by the person. This would normally be protected by a host, such that the pod could be effectively offline.

If someone wants, then they host the whole lot themself, acting as their own host, and managing their own pod.

Otherwise, they will run their pod on a trusted host, which will collect their messages and invoke their pod in a secure manner.

A pod is a data store and execution environment, intended to be run in a way that keeps all details firmly inside a container at all times.

## Use cases

### Messaging

Basically like email, except fully encrypted and unreadable from outside the pod or something securely connected to it. User can manage by sending a message to their pod, instructing it to connect out to their client.

### Calendar

A user stores their calendar in their pod, where it is a accessible from any authorised client. User can manage by sending a message to their pod, instructing it to connect out to their client.

### Banking

A bank allows its customers to approve transactions by sending machine readble messages to the user, and not continuing until a response arrives.

## Protocols

Message formatting, encryption, transfer, processing, etc.

## Components

None of which are directly required, the protocols are the important things.

### Gateway

Gateway for sending messages. Implements a client facing protocol.

### Host

Manages and invokes pods. Implements a mail-box protocol.

### Registry

Makes it possible to define where a pod is. Implements a registry protocol.

### Router

Store-and-forward messaging, doing its best to get messages through. Implements a forwarding protocol.

## Sample things

### pod1

A pod.

### svc1

A service that uses messaging as part of its operation.

### client1

A client (user agent) that a user might use to communicate with her own pod.
