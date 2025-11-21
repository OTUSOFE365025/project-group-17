<h2>Step 2: Establish Iteration Goal </h2>
The goal of this iteration is to identify and define sructures that directly support the primary use cases, and these include:
UC-1
UC-2
UC-3
UC-4

<h2>Step 3: Choose Elements of the System to Refine</h2>
In this iteration we will focus on refining the core structural elements needed to establish the basic structure for AIDAP.

<h2>Step 4: Choosing Design Concepts That Satisfy the Selected Drivers</h2>

<table>
  <tr>
    <td><strong>Design Decision</strong></td>
    <td><strong>Rationale</strong></td>
  </tr>

  <tr>
    <td><strong>Refine the Rich Internet Application (RIA) Frontend</strong></td>
    <td>
      The RIA frontend continues to be the best approach for supporting reactive, accessible,
      and device-independent UI behaviour. It enables dynamic page updates using AJAX,
      supports screen readers, and ensures consistent behavior across multiple device types.
      These refinements will help us shape the login interface, monitoring dashboards,
      and administrative panels. (UC-1, UC-2, UC-3, CON-1, CON-3, CRN-1)
    </td>
  </tr>

  <tr>
    <td><strong>Refine the Service-Based Application Backend</strong></td>
    <td>
      We extend the backend by assigning more specific responsibilities to the core services.
      Separating authentication, metric processing, and user-role administration keeps the
      backend modular, secure, and easier to maintain as the application grows. (UC-1, UC-2, UC-3, CRN-3, QA-1)
    </td>
  </tr>

  <tr>
    <td><strong>Apply the Four-Tier Deployment Structure</strong></td>
    <td>
      We reuse and refine the four-tier structure introduced earlier by clearly mapping 
      each use case to the Client, API, Logic, and Database tiers. This structure increases
      security by isolating sensitive logic from public UI requests and allows clean routing
      for sign-in, monitoring, and administrative workflows. (UC-1, UC-2, UC-3, QA-2, QA-1, CON-4)
    </td>
  </tr>

  <tr>
    <td><strong>Use the Spring Framework for Module Definition</strong></td>
    <td>
      Spring remains the foundation for defining backend modules. Its built-in authentication
      tools support SSO, while Spring Boot helps formalize metric retrieval. Dependency injection
      simplifies service wiring, and Spring’s modular structure positions AIDAP for future AI
      capabilities. These refinements improve maintainability and scalability across the system. (UC-1, UC-2, UC-3, QA-3, QA-4, CON-4)
    </td>
  </tr>

</table>
   

<h2>Step 5: Element Instantiation, Responsibilities, and Interface Definition</h2>

<table>
  <tr>
    <td><strong>Module</strong></td>
    <td><strong>Description</strong></td>
  </tr>

  <tr>
    <td><strong>Authentication & Role-Management Module</strong></td>
    <td>
      This module will handle all sign-in activity, manage user roles, and enforce access control.
      It ensures users are authenticated through SSO, their actions can be traced, and each role
      only has access to the features they're authorized to use. (UC-1, UC-3, QA-1)
    </td>
  </tr>

  <tr>
    <td><strong>Operational Monitoring Module</strong></td>
    <td>
      This module will provide the system maintainer with a dashboard that shows real-time metrics
      and the current health of different parts of the application. This will help maintainers track
      performance, identify issues early, and ensure the system stays available and stable. (UC-2)
    </td>
  </tr>

  <tr>
    <td><strong>Personalization Module</strong></td>
    <td>
      This module will store each user's personal preferences, such as their chosen language,
      conversation style, UI mode, and notification settings. It supports a more tailored
      user experience and allows the platform to adapt to individual needs over time. (UC-4, QA-5)
    </td>
  </tr>

</table>

<h2>Step 6: Sketch Views and Record Design Decisions</h2>
<h3>UC-1</h3>
<img width="618" height="686" alt="image" src="https://github.com/user-attachments/assets/1f1c8e3c-21d6-461c-8847-899aa65ee5b8" />
<h3>UC-2</h3>
<img width="738" height="702" alt="image" src="https://github.com/user-attachments/assets/67bacfc8-c614-4de6-b843-2815580e2952" />
<h3>UC-3</h3>
<img width="653" height="675" alt="image" src="https://github.com/user-attachments/assets/a5eee562-cc1f-4556-a9a1-e1f764ee474c" />

<img width="659" height="829" alt="image" src="https://github.com/user-attachments/assets/1441ca80-4adb-44d4-946d-24c471303325" />

<img width="678" height="549" alt="image" src="https://github.com/user-attachments/assets/2846d755-4d5e-4ef3-984a-cf39a7a0df8e" />

<img width="569" height="383" alt="image" src="https://github.com/user-attachments/assets/1fbecf13-32f7-4629-97a3-24ef29f8113e" />


<h2>Step 7:  Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose</h2>

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
|---------------|----------------------|-----------------------|--------------------------------------------|
|               |               |           UC-1              | Built authentication module.
|        |                      |      UC-2                    | Built Maintainer Module.                                         |
|          |                      |     UC-3                   | Authenticator module has role-based authentication.                                          |
|          |       UC-4                |                       | Notification module is started however it is a low priority.                                            |
|          |        UC-5                  |                    | AI framework is started, but a low priority while building system.                                          |
|               | UC-6 |                                       | This will use the same notification system as UC-4 |
|               | QA-1                |                       | No additional specific decisions made. |
|               | QA-2                |                       | No additional specific decisions made.
|               |      QA-3                |                       | Development of the RIA and the spring framework improve usability.                       |
|             |    QA-4             |                               |  The modularity of the four-tier deployment and the spling framework make maintaining the system quick and easy with little downtime.     |
|          |         QA-5              |                        |  Development of th epersonalization module improves adaptability.                   |
| QA-6          |                      |                       | No relevant decisions made.                       |
|               | CON-1               |                       | No additional specific decisions made. |
|            CON-2 |               |                       |  No relevant decisions made. |
|               | CON-3               |                       | No additional specific decisions made. |
|               | CON-4               |                       | No additional specific decisions made. |
|               | CRN-1               |                       | No additional specific decisions made. |
|         |       CRN-2                |        | A strong deployment and framework help dampen the load of peak times.    |
|         |              |           CRN-3              | No additional specific decisions made. |
|       CRN-4        |                 |                       |  No relevant decisions made. |
