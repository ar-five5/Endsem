# Software Engineering - Lecture 10.1

## Slide 1: Software Engineering(CS3201)Additional material – Arch. Patterns and Estimation

Avinash

## Slide 2

Architectural patterns – Microservices, Peer to Peer and Event based
2
Software Engineering

## Slide 3: Micro service architecture

Application consists of small, independent services that communicate with one another to get the task done
Each service is responsible for a particular function
Each service can be developed, deployed and maintained independently
  - Teams can work on a particular service, fix bugs, release new versions, without effecting the rest of the services
Each microservice handles one specific responsibility
Each microservice can have its own technology (programming language, DB, frameworks) different from other services
Each microservice has its own DB
Microservices communicate with one another over the network
Can scale up any service as needed (payments service can be scaled up at start of semester)
3
Software Engineering

## Slide 4: Micro service architecture: ex. Netflix

Key services in Netflix:
  - User service – manages user data, profiles and settings
  - Auth service – manages login, session, token validation
  - Content service – stores content (shows, movies) metadata/ description
  - Recommendation service – generates recommendations based on history
  - Playback service – streams video content, selects CDN nodes (CDN – Content Delivery Network, caches data to be streams over several servers, you get your data from the server nearest to you)
  - Billing service – handles subscriptions / payments
  - Search service – handles searching in content library
  - Notifications service – send push notifications to users
Each service is deployed independently, communicates using APIs and usually runs in containers like Docker (organized by Kubernetes)
4
Software Engineering

## Slide 5: Micro service architecture: ex. Netflix

How all these key services communicate?
  - REST APIs or gRPC
  - Asynchronous messaging queues (e.g., Apache Kafka)
  - Service Discovery with tools like Eureka
  - Load balancing via Ribbon
REST APIs – resources accessed and manipulated via standard HTTP protocols(GET, POST, PUT, DELETE, …)
gRPC – open-source RPC
Apache Kafka – keyword here is async, services communicate via queues, do not busy wait
Eureka – A service registry that helps discover services
Ribbon – Help balance load among several instances of a service
5
Software Engineering

## Slide 6: Micro service architecture: ex. Netflix

When user hits PLAY
  - Auth Service - checks if you're logged in and have access.
  - User Service - loads your profile.
  - Content Service - fetches movie metadata.
  - Recommendation Service - tweaks the interface.
  - Playback Service - starts streaming from the closest server (CDN).
  - Rating Service - tracks what you watch and how you rate it later.
  - Analytics/Logging Services - track your interaction for future improvement.
6
Software Engineering

## Slide 7: Peer to Peer Architecture

Decentralized network architecture (as opposed to Client-Server)
Consists of computers, called peers, where each computer has equal status and can act as both client and server
Every peer can request for resources and provide resources
No central server controlling network, peers communicate directly with one another (instead of having to communicate via server)
Main features:
  - Decentralized
  - Equal roles /capabilities
  - Resource sharing: by product of decentralization
  - Scalability
7
Software Engineering

## Slide 8: Peer to Peer: example Bit torrent (file sharing)

Imagine you want to download a movie using torrents
  - Download a .torrent file or using magnet link
  - This file contains metadata (file name, structure, tracker info)
  - Tracker - a lightweight server that helps a peer find other peers who have the file or parts of it
  - The peer then connects to one or more peers who have the file
  - Types of peers – seeders (who have the complete file), and leechers (who have some parts of the file – they are probably downloading at this point)
  - The peer downloads from several other peers simultaneously
  - The parts of file you download, you start uploading them to others in need
  - Once you have completed downloading, your entire file is ready, and you continue uploading file parts to others who need
8
Software Engineering

## Slide 9: Peer to Peer: example Bit torrent (file sharing)

Roles
  - Peer (network participant)
    - Seeder
    - Leecher
  - Tracker (keeps track of peers sharing the same file)
Advantages of P2P
  - High speeds (multiple sources)
  - No central server (one point of attack/ vulnerability/ power-authority)
  - Efficient
  - Scalable
Disadvantages
  - No guaranteed uptime / availability (peers can go offline anytime)
9
Software Engineering

## Slide 10: Event based Architecture

Listener pattern (or observer pattern) is an example of event-based architecture – recall last class (Lec 9.1)
10
Software Engineering

## Slide 11

Software cost estimation - COCOMO
11
Software Engineering

## Slide 12: COCOMO (Hans Van Vliet, pg. 155)

COnstructive COst MOdel (COCOMO) is one of the best documented algorithmic cost estimation models
Simplest form – Basic COCOMO, a formula that relates effort (cost) to software size
  - E = bKLOCc
  - where b and c are constants that depend on the kind of project being executed
COCOMO distinguishes three classes of projects:
  - Organic – small team, good experience, known environment and seldom large projects
  - Embedded – inflexible environment, many constraints, large project
  - Semidetached – experienced and inexperienced people, semi large project
12
Software Engineering

## Slide 13: COCOMO

Parameters for the three project types:
  - organic: b = 2.4, c = 1.05
  - semidetached: b = 3.0, c = 1.12
  - embedded: b = 3.6, c = 1.20
Example of estimation:
Here, one man-month is an
estimate of effort, and
equals effort of one man
for a month
13
Software Engineering

## Slide 14: Intermediate and Detailed COCOMO

Advanced COCOMO models that take into account 15 cost drivers – attributes that effect productivity, and hence cost
These models add a multiplicative correction factor to effort estimate
These models use a value of b slightly different from basic COCOMO
Suppose we find a nominal effort of basic COCOMO as 40 man-months, but complexity of the software is low, a multiplicative factor of 0.85 can be considered, and therefore correct the man-months as 0.85 * 40 = 34 months
You may consider Basic COCOMO to generate nominal values of effort
14
Software Engineering

## Slide 15: Design Patterns: Sample

15
Software Engineering

## Slide 16: Design Patterns: Sample

16
Software Engineering

## Slide 17: Difference between design and arch. pattern?

17
Software Engineering

## Slide 18

Implementation Issues
18
Software Engineering

## Slide 19: Implementation Issues

Reuse
Configuration Management
Host-target development
19
Software Engineering

## Slide 20

Open-source Development
20
Software Engineering
