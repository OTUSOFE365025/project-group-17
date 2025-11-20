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
      and administrative panels. <br><br>
      <em>(UC-1, UC-2, UC-3, CON-1, CON-3, CRN-1)</em>
    </td>
  </tr>

  <tr>
    <td><strong>Refine the Service-Based Application Backend</strong></td>
    <td>
      We extend the backend by assigning more specific responsibilities to the core services.
      Separating authentication, metric processing, and user-role administration keeps the
      backend modular, secure, and easier to maintain as the application grows. <br><br>
      <em>(UC-1, UC-2, UC-3, CRN-3, QA-1)</em>
    </td>
  </tr>

  <tr>
    <td><strong>Apply the Four-Tier Deployment Structure</strong></td>
    <td>
      We reuse and refine the four-tier structure introduced earlier by clearly mapping 
      each use case to the Client, API, Logic, and Database tiers. This structure increases
      security by isolating sensitive logic from public UI requests and allows clean routing
      for sign-in, monitoring, and administrative workflows. <br><br>
      <em>(UC-1, UC-2, UC-3, QA-2, QA-1, CON-4)</em>
    </td>
  </tr>

  <tr>
    <td><strong>Use the Spring Framework for Module Definition</strong></td>
    <td>
      Spring remains the foundation for defining backend modules. Its built-in authentication
      tools support SSO, while Spring Boot helps formalize metric retrieval. Dependency injection
      simplifies service wiring, and Spring’s modular structure positions AIDAP for future AI
      capabilities. These refinements improve maintainability and scalability across the system. <br><br>
      <em>(UC-1, UC-2, UC-3, QA-3, QA-4, CON-4)</em>
    </td>
  </tr>

</table>
   

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
