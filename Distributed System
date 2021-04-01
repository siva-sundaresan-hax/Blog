## Why are the Russians good at developing Distributed Systems?

I’m back with another blog post, and this time I want to share my experiences of working with large-scale distributed systems! I want to highlight what I feel an architect/developer should focus on when dealing with a Distributed system and how’d one test the same.
Let’s start with the definition of a Distributed system. Per wiki,
> A distributed system is a system whose components are located on different networked computers, which communicate and coordinate their actions by passing messages to one another from any system.

In other words, a distributed system does not have a single point failure. It is usually set up in multiple data centers. Data is replicated back and forth amongst these D.C. deployments, and the application deployed in any single D.C. can act as a source of truth!

## C.A.P. theorem
The cornerstone for any distributed system is its foundation on C.A.P. theorem. Let’s dive into what the theorem is all about. Again going back to the wiki,
In theoretical computer science, the C.A.P. theorem, also named Brewer’s theorem after computer scientist Eric Brewer, states that it is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees:[1][2][3]
- Consistency: Every read receives the most recent write or an error
- Availability: Every request receives a (non-error) response, without the guarantee that it contains the most recent write
- Partition tolerance: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.

In other words, when developing a Distributed system, only 2 out of the three guarantees can be honored.
Let’s look into each of them in little more detail.
### Consistency
Consistency deals with the fundamental idea of the “state” of the resource being read or modified in different nodes of a distributed system. When you are developing a consistent system, for example, a financial system, it is critical that “the state,” for instance, the account balance is identical across all the nodes of a distributed system! Conversely, there are use cases of an “eventual consistency” model. Here the data is replicated to different nodes of the distributed system, and often, the origin node, where the change is occurring on a resource, is the initiator of the state change. The “change” is then propagated to other nodes in the system, usually through a replication mechanism. If you’ve worked with systems involving Database replication like Postgres or even the (NoSQL) Cassandra, for that matter, you must be familiar with this concept.
### Availability
This deals with guaranteed uptime! While architecting a Distributed system, it is critical not to have a Single point of failure — Wikipedia and defensive software architecture such as HA, Observability, slow logs in DB, etc., must be put in place to ensure (close to) 100% uptime of the application.
### Partition tolerance
Partition tolerance deals with the classical “split-brain” problem. As an architect, you should have questions like the following in your mind while dealing with Partition tolerance. How resilient is the system when there is a network failure? When developing an eventually consistent system, how does the system handle network or disk failures? Have you implemented a replay/catchup mechanism? Answers to these questions will help an architect with a high-level list of techniques for ensuring the system is guarded against Partition tolerance.
### Testing a Distributed System
As you might have realized by now, testing a Distributed System can present its challenges. Having worked on such large-scale systems, here’ my checklist of the way I approach testing Distributed system. I don’t claim this to be a comprehensive list for all the use cases, but this will give you a good starting point. With that said, here’s a high-level checklist for designing test automation for a Distributed system.
Functional testing of the APIs/microservices deployed on individual nodes.
Testing for consistency/eventual consistency in the replication layer.
Performance and Scale testing of the entire Distributed setup.
Security testing(static code analyzers, port scanning, Pen testing etc.) of the infrastructure hosting the Distributed application.
Chaos testing of the infrastructure to explore inconsistent states in the system.
Now onto the most important question of this post, 
> Why are Russians, the best in the world, when it comes to developing Distributed systems? 
Because …
> They are from Russia. Naturally, they know a thing or two about Distribution ;) #SovietUnion

<Plug: If you like clean, tech related humor, do checkout #SivaStandupJokes in [LinkedIn](https://www.linkedin.com/feed/hashtag/sivastandupjokes/) and [Twitter](https://twitter.com/hashtag/sivastandupjokes) >

