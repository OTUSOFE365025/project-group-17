<h2>Step 2: Establish Iteration Goals by Selecting Drivers</h2>
For this iteration, we would like to focus on QA-2, availability:

The system should remain operational and accessible 99.5% of the time or higher. Scheduled maintenance should cause minimal disruption, and automatic failover mechanisms should recover from crashes or downtime instantly to maintain continuous service availability.

This iteration will also have a slight focus on QA-6, performance efficency:

Queries and notifications should be processed and displayed within seconds, even under high system load. The system should optimize network and server performance to maintain quick response times, ensuring uninterrupted interaction for all users.

These two go hand in hand, as a more efficent program will result in less downtime from performance related issues.


<h2>Step 3: Choose one or more elements of the system to refine</h2>
For this iteration, we will be refining two physical nodes, the application server and the database server.

<h2>Step 4: Choose one or more design concepts that satisfy the selected drivers</h2>


| **Design Decision** | **Rationale** |
|---------------------|---------------|
Implement the active redundancy tactic | Implementing active redundancy will allow the system to run with caching and load balancing design concepts, preventing server overload craches while improving efficency, and creating multiple servers the application can run on in the event of a crash. The active redundancy tactic will give us the quickest restoration time, fulfiling QA-2's requirement of near instant recovery. |


<h2>Step 5: Instatiate architectural elements and responsibilities</h2>

| **Design Decision** | **Rationale** |
|---------------------|---------------| 
Implement a cache-aside caching system | A cache-aside system checks cache first, then queries the DB if requested answers are not found in cache. Frequently used data such as commonly asked questions, exam schedules and course schedules may be kept in cache to reduce DB load. Althought the first uses of the system may be slow as it learns what common questions are, over time db load will be lowest compared to other caching systems. The cache-aside system is also the lightest caching system, requiring no extra writes to function and only saving frquently used data, unlike write-through caching. (QA-2, QA-6) |
|Implement weighted round-robin load balancing | Servers are given requests and queries in order, based upon a weight value determined by capacity. With emptier servers reciving more requests, the chances of one server slowing down or crashing is severely reduced. User sessions will have varying weight depending on complexity of question as well as if they require follow ups. Weighted round-robin was a better fit then least connections load balancing as chatbot connections can vary in their resource demands. (QA-2, QA-6) |

<h2>Step 6: Sketch Views and Record Design Decisions</h2>


<h2>Step 7:  Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose</h2>

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
|---------------|----------------------|-----------------------|--------------------------------------------|
|               |               |           UC-1              | No additional specific decisions made.
|        |                      |      UC-2                    | No additional specific decisions made.                                       |
|          |                      |     UC-3                   | No additional specific decisions made.                                      |
|          |       UC-4                |                       | No additional specific decisions made.                                          |
|          |        UC-5                  |                    | No additional specific decisions made.                                         |
|               | UC-6 |                                       | No additional specific decisions made.|
|               | QA-1                |                       | No additional specific decisions made. |
|               | QA-2                |                       | Caching and load balancing systems will further reduce downtime.
|               |      QA-3                |                       | No additional specific decisions made.                  |
|             |    QA-4             |                               |  No additional specific decisions made.  |
|          |         QA-5              |                        |  No additional specific decisions made.             |
|          |        QA-6               |                       | Specific design concepts were chosen that are light on the system while still performing theyre required duties.                      |
|               | CON-1               |                       | No additional specific decisions made. |
|            CON-2 |               |                       | No additional specific decisions made.|
|               | CON-3               |                       | No additional specific decisions made. |
|               | CON-4               |                       | No additional specific decisions made. |
|               | CRN-1               |                       | No additional specific decisions made. |
|         |       CRN-2                |        | No additional specific decisions made.  |
|         |              |           CRN-3              | No additional specific decisions made. |
|       CRN-4        |                 |                       |  No additional specific decisions made. |
