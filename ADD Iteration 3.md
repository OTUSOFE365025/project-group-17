<h2>Step 2: Establish Iteration Goals by Selecting Drivers</h2>
For this iteration, we would like to focus on QA-2, availability:

The system should remain operational and accessible 99.5% of the time or higher. Scheduled maintenance should cause minimal disruption, and automatic failover mechanisms should recover from crashes or downtime instantly to maintain continuous service availability.

This iteration will also have a slight focus on QA-6, performance efficency:
Queries and notifications should be processed and displayed within seconds, even under high system load. The system should optimize network and server performance to maintain quick response times, ensuring uninterrupted interaction for all users.

These two go hand in hand, as a more efficent program will result in less downtime from performance related issues.


<h2>Step 3: Choose one or more elements of the system to refine</h2>
For this iteration, we will be refining two physical nodes, the application server and the database server.

<table>
  <thead>
    <tr>
      <th>Design decisions</th>
      <th>Rationale</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td><strong>Step 4: Choose one or more design concepts that satisfy the selected drivers</strong><br><br>
      1: Implement the active redundancy tactic.</td>

      <td>
      Implementing active redundancy will allow the system to run with caching and load balancing design concepts,
      preventing server overload craches while improving efficency, and creating multiple servers the application can run on
      in the event of a crash. The active redundancy tactic will give us the quickest restoration time, fulfiling QA-2's requirement
      of near instant recovery.
      </td>
    </tr>
  </tbody>
</table>

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
