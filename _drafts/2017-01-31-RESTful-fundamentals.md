---
published: false
---
https://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm

Environments concerns : 
- Network reliability 
- Latency 
- Bandwidth
- Security
- Network topology 
- Administrator 
- Transport cost (like support network cost)
- Heterogeneous network 
- Complexity 

Architecture constraint to address environments concerns: 
- Separation of concerns (benefits: portability, scalability, evolvability)
- Stateless (is about communication, state is explicit; benefits: visibility, reliability, scalability)
- Cache (responses need to be marked as cacheable or non-cacheable; benefits: efficiency, scalability, performance)
- Uniform Interface (benefits: visibility, evolvability)
- Layered System (a component in a solution can only communicate with components from the same layer; benefits: scale, manageability)
- Code-On-Demand 


Uniform Interface

- Components by role :
	- Origin Server
	- User Agent
	- Gateway (multi origin server )
	- proxy (multi user agents)
- Connectors by type
	- Client (initiate a req)
	- Server (listen for a req)
	- Cache (manage a store of representation)
	- Resolver (translates a resource identifier)
	- Tunnel (realize communication across a boundary)

- Uniform Interface format: 
	- Resource
	- Resource Identifier
	- Resource Metadata (eg: Location header(resource identifier), ETag(state of resource at a point in time))
	- Representation Metadata (like: media preferences)
	- Representation
		- Server driven content negation
		- Agent driven  content negation
	- Hypermedia!!! (main difference between REST and RPC)


Design REST APIs (Services):
	1) List requirements
	2) Identify state transitions
		- solution and resource state
		
	3) Identify resource
	4) Design media type
		- base format (XML, JSON, HTML, etc)
		- state transfer (Read only, predefined, Adhoc)
		- domain style (Specific, General, Agnostic)
		- application flow (None, intrinsic, Applied)

Read about Mapping to base formats, representation format and media type

Design REST APIs (Clients):
	- Review media types (documentation and samples, request a test resource)
	- 