

- Easiest way to sabotage your system design interview is to fail to deliver a working system, so focus on the right thing

### 1. Requirements (~5 minutes)
==The goal of this section is to get a clear understanding of the system that you are being asked to design.==
1. **Functional Requirements**: the "Users/Clients should be able to..." statements
	- Should be the first thing discussed
	- This is usually a back and forth, so ask targeted questions to arrive at a prioritized list of core features
	- For example, for designing a system like Twitter:
		- Users should be able to post tweets
		- Users should be able to follow others
		- Users should be able to see tweets from users they follow
	- `Keep requirements targeted. Prioritize to 3. You are evaluated on your ability to focus on what matters`
2. **Non-functional requirements**: statements about the system qualities that are important to your users. These can be phrased as "The system  should be able to..."
	- For example, for designing a system like Twitter:
		- The system should be high availability, prioritizing availability over consistency
		- The system should be able to scale to support 100M+ DAUs
		- The system should be low latency, rendering feeds in under 200ms
	- `Try to quantify these requirements`
	- Here is a checklist of things to consider to help identify the most important non-functional requirements. 
		- [[CAP Theorem]] - Should your system prioritize consistency or availability?
		- Environment Constraints - Are there any constraints on the environment in which your system will run?
		- [[Scalability]] - Does this system have unique scaling requirements? Consider reader vs writer ratio here. Does your system need to scale reads or writes more?
		- [[Latency]] - How quickly does the system need to respond to user requests?
		- [[Durability]] - How important is it that the data in your system is not lost? For example, a social media platform might be able to tolerate some data loss, but a banking system cannot
		- [[Security]] - How secure does the system need to be? 
		- [[Fault Tolerance]] - How well does the system need to handle failure?
		- [[Compliance]]
3. **Capacity Estimation** (Skip for now)

### 2. Core Entities (~2 minutes)
Take a moment to identify and list the core entities of your system. These are the core entities that your API will exchange and that your system will persist in a Data Model. 
- In an actual interview, just jot down a bulleted list and explain this is your first draft

For example, for Twitter:
- User
- Tweet
- Follow

### 3. API or System Interface (~5 minutes)
Before you get into the high-level design, you'll want to define the contract between your system and its users. Oftentimes, this maps directly to the functional requirements you've already identified. 

`You have a decision to make here about RESTful API or GraphQL API`

For example, for Twitter:
- POST /tweet
	- body: 
		- "text": string
- POST /follow/:userId
- GET /tweets/:tweetId -> Tweet
- GET /feed -> Tweet[]
- `Notice how there is no user id in the POST endpoint. This is because we will get the id from the auth token in the request header. Don't put sensitive info in the body`

### 4. Data Flow (optional)
### 5. High Level Design (~10-15 minutes)
Now that you have a clear understanding of the requirements, entities, and API of your system, you can start designing the high-level architecture. 
- This is where you draw boxes and arrows to represent the different components of your system and how they interact

### 6. Deep Dives
With the remaining time, you need to harden your design by (a) ensuring it meets all of your non-functional requirements (b) addressing edge cases (c) identifying and addressing all issues and bottlenecks and (d) improving the design based on probes from your interviewer

![[Pasted image 20250629224809.png]]