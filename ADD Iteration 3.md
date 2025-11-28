<h2>Step 2: Establish Iteration Goals by Selecting Drivers</h2>
For this iteration, we would like to focus on QA-2, availability:

The system should remain operational and accessible 99.5% of the time or higher. Scheduled maintenance should cause minimal disruption, and automatic failover mechanisms should recover from crashes or downtime instantly to maintain continuous service availability.

This iteration will also have a slight focus on QA-6, performance efficency:
Queries and notifications should be processed and displayed within seconds, even under high system load. The system should optimize network and server performance to maintain quick response times, ensuring uninterrupted interaction for all users.

These two go hand in hand, as a more efficent program will result in less downtime form performance related issues.


<h2>Step 5: </h2>
1: Introduce caching and load balancing.

Keeping frequently asked questions as well as relevant information to the conversation
in the cache will reduce response times greatly by reducing database queries.
Load balancing will reduce the chances of a single server being overloaded during
peak times such as students requesting their exam schedules around exam season.
It will also increase throughput by having multiple servers to connect to and respond through.
(QA-2, QA-6)
