Step 2: Establish Iteration Goal
The goal of this iteration is to identify and define sructures that directly support the primary use cases, and these include:
UC-1
CRN-1
CON-1
CON-3

Step 3: Choose Elements of the System to Refine
In this iteration we will focus on refining the core structural elements needed to establish the basic structure for AIDAP.

Step 4: Choosing Design Concepts that satisfy the selected drivers
<h2>Step 4: Choosing Design Concepts That Satisfy the Selected Drivers</h2>

<table>
  <tr>
    <td><strong>Design Concept</strong></td>
    <td><strong>Rationale</strong></td>
    <td><strong>Supported Drivers</strong></td>
  </tr>

  <tr>
    <td><strong>Refining the Rich Internet Application (RIA) Frontend</strong></td>
    <td>
      This iteration refines the RIA introduced in Iteration 1 by focusing on how it supports the primary system workflows. 
      The RIA enables responsive input validation, dynamic updates using AJAX, accessibility hooks for screen readers, and consistent 
      multi-device behavior. These improvements support the UI components required for sign-in, monitoring dashboards, and 
      user-management panels.
    </td>
    <td>CON-1, CON-3, CRN-1, UC-1, UC-2, UC-3</td>
  </tr>

  <tr>
    <td><strong>Refining the Service-Based Application Backend</strong></td>
    <td>
      The service-backend structure is expanded by assigning responsibility to modules that directly support the three primary use cases. 
      AuthenticationService manages credential verification and session creation, MetricsService retrieves and processes system performance data, 
      and UserAdminService handles user roles and permissions. This refinement ensures a modular and secure backend by separating 
      UI logic from sensitive operations.
    </td>
    <td>CRN-3, UC-1, UC-2, UC-3, QA-1</td>
  </tr>

  <tr>
    <td><strong>Applying the Four-Tier Deployment Structure</strong></td>
    <td>
      The four-tier structure (Client → API → Logic → Database) is now aligned with workflow behavior. The client layer handles 
      dynamic UI actions, the API layer routes sign-in, monitoring, and administrative requests, the logic layer performs validation 
      and auditing, and the database layer stores users, metrics, sessions, and logs. This ensures isolation between public UI 
      requests and sensitive backend processes while improving system reliability.
    </td>
    <td>QA-2, QA-1, CON-4, UC-2, UC-3</td>
  </tr>

  <tr>
    <td><strong>Using the Spring Framework for Module Definition</strong></td>
    <td>
      Spring is further refined in this iteration to support the system’s structural requirements. Spring Security provides authentication flows, 
      Spring Boot services formalize metrics retrieval, dependency injection simplifies controller-service wiring, and Spring’s modular design 
      prepares AIDAP for future AI extensions. This strengthens security, maintainability, and scalability.
    </td>
    <td>CRN-3, QA-4, CON-4, UC-1, UC-3</td>
  </tr>

</table>
   

STEP 5:

<h2>Step 5: Element Instantiation, Responsibilities, and Interface Definition</h2>

<h2>Step 5: Element Instantiation, Responsibilities, and Interface Definition</h2>

<table>
  <tr>
    <td><strong>Module</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Supported Drivers</strong></td>
  </tr>

  <tr>
    <td><strong>Authentication & Role-Management Module</strong></td>
    <td>
      This module will handle all sign-in activity, manage user roles, and enforce access control.
      It ensures users are authenticated through SSO, their actions can be traced, and each role
      only has access to the features they're authorized to use.
    </td>
    <td>UC-1, UC-3, QA-1</td>
  </tr>

  <tr>
    <td><strong>Operational Monitoring Module</strong></td>
    <td>
      This module will provide the system maintainer with a dashboard that shows real-time metrics
      and the current health of different parts of the application. This will help maintainers track
      performance, identify issues early, and ensure the system stays available and stable.
    </td>
    <td>UC-2</td>
  </tr>

  <tr>
    <td><strong>Personalization Module</strong></td>
    <td>
      This module will store each user's personal preferences, such as their chosen language,
      conversation style, UI mode, and notification settings. It supports a more tailored
      user experience and allows the platform to adapt to individual needs over time.
    </td>
    <td>UC-4, QA-5</td>
  </tr>

</table>
