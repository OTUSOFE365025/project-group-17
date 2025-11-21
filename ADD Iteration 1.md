<h1>Iteration 1</h1>

<h2>Step 1: Confirm Inputs</h2>

Design Purpose:
This is a greenfield system for a university environment. The purpose is to create a detailed architectural design for an AI-powered digital assistant platform (AIDAP) that supports students, staff, and lecturers while remaining secure, available, and accessible across devices.

Primary Functional Requirements (Use Cases):
The primary use cases for this iteration are:

UC1: Student Sign-In 

UC2: System Maintainer Monitors Performance 

UC3: Managing Users

These use cases must be implemented first to ensure the platform functions correctly and securely.
The AI and feature implementation will be included in future iterations once a structure is created.

Quality Attribute Scenarios:
Selected quality attributes for this iteration (drivers):

Security & Traceability: High importance, High difficulty, associated with UC1 and UC3

Availability: High importance, High difficulty, associated with UC2, UC4, UC6

Usability: Medium importance, Medium difficulty, associated with UC1, UC4, UC5

Maintainability: High importance, Medium difficulty, associated with UC3, UC2, UC6

Adaptability/Personalization: Low importance, Medium difficulty, associated with UC1, UC4, UC5

Performance Efficiency: High importance, High difficulty, associated with UC4 and UC5

Selected drivers for this iteration: Security & Traceability, Availability, Maintainability, Performance Efficiency. These directly support the primary functional requirements.

Constraints:

CON-1: Multi-device and multi-OS support

CON-2: Support for high concurrency (50 admin sessions, 5000 user sessions)

CON-3: Accessibility compliance (screen readers, text-to-speech)

CON-4: Data encryption, access control, and auditing

Concerns:

CRN-1: Reactive UI across devices and accessibility

CRN-2: Peak load estimation and scalability

CRN-3: Modular system for university ecosystem

CRN-4: Minimize data loss and downtime through backups


<h2>Step 2: Establish Iteration Goal by Selecting Drivers</h2>

Since the AIDAP is a greenfield system, its important to establish structure as soon as possible.

We will focus on drivers related to structure:

UC-1
CRN-1
CON-1
CON-3

These five drivers outline a basic structure and starting point for our design.
Although these are our priority, other drivers are still important and may be adressed.


<h2>Step 3: Choose Elements of the System to Refine</h2>

We are going to focus on refiing the basic structure we need to create from scratch.
<img width="638" height="359" alt="image" src="https://github.com/user-attachments/assets/045f2d1a-45af-49ee-a2d0-a17c9c2a31c4" />



<h2>Step 4: Choose Design Concepts That Satisfy Selected Drivers</h2>

| Design Decision | Rationale              
|--------------|-----------------------------------------
| Use a Rich Internet Application frontend | RIAs will support a reactive and accessible UI across various devices. Using AJAX and other web technologies to update the page without refreshing the page, relying less on a good connection. RIAs also favor cloud databases instead of local storage, and with a centralized server and database running the application, RIAs fit best. RIAs provide a smooth user expeience while keeping the application within a browser, perfect for an AI chatbot. (CON-1, CON-3, CRN-1)
| Use a Service application backend | A service application backend will increase modularity and seperate business logic from UI, increasing security. Service application backends are perfect as this type of reference architechture works best when humans are not involved. (CRN-3, UC-1, UC-6)
| Use a four tier deployment structure | Having a four tier deployment structure of client, api, logic and database increases security, letting the application logic reside within a protected and private network while having the web application on a open public network. Considering many students could be asking sensitive questions about their academics including their standing or requests for support, having the logic and data be decoupled an additional level is important. (QA-2, QA-1, CON-4)
| Use the Spring Framework | The Spring framework is a good choice for an AI web app. With easy integration with other frameworks as well as the recent release of the Spring AI extension for natural language understanding, modularity and ease of maintainance are two main benefits. Spring Security also supports our SSO sign in, encrypted communication and role-based access control. Spring's dependancy inversion approach also makes testing throughout the development cycle easier. (CRN-3, CON-4, UC-1)


<h2>Step 5: Instantiating Architectural Elements, Responsibilities, Interfaces</h2>

| Design Decision | Rationale              
|--------------|-----------------------------------------
|Remove all local data storage from the client |  Ensures encrypted data stays on secure servers. (CON-4)
|Create module bases to build application functionality | Creating a modular system that is expandible is of the utmost importance for this project. Taking advantage of the Swing Framework's modules and the Service Architecture back-end will create an outline of a seamless and responsive app. (CRN-3)


<h2>Step 6: Sketch Views and Record Design Decisions</h2>

<img width="465" height="812" alt="image" src="https://github.com/user-attachments/assets/2ba0b550-2813-458a-a367-33af9557d011" />

<img width="672" height="555" alt="image" src="https://github.com/user-attachments/assets/3c24c63b-cdc0-474f-add4-352b0534468f" />




<h2>Step 7:  Perform Analysis of Current Design and Review Iteration Goal and Achievement of Design Purpose</h2>

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
|---------------|----------------------|-----------------------|--------------------------------------------|
|               | UC-1                |                       | Selected reference architecture identifies components that will support this functionality. |
| UC-2          |                      |                       | No relevant decisions made.                                           |
| UC-3          |                      |                       | No relevant decisions made.                                            |
| UC-4          |                      |                       | No relevant decisions made.                                            |
| UC-5          |                      |                       | No relevant decisions made.                                            |
|               | UC-6                |                       | Selected reference architecture identifies components that will support this functionality. |
|               | QA-1                |                       | Spring Security and backend separation support secure access and traceability. |
|               | QA-2                |                       | Four-tier deployment provides foundation for redundancy and uptime. |
| QA-3          |                      |                       | No relevant decisions made.                                            |
| QA-6          |                      |                       | No relevant decisions made.                                            |
|               | CON-1               |                       | RIA structure supports multi-device access. |
| CON-2         |                      |                       | No relevant decisions made.                                            |
|               | CON-3               |                       | RIA structure supports accessibility considerations. |
|               | CON-4               |                       | Centralized backend and encrypted communication supported through Spring. |
|               | CRN-1               |                       | RIA architecture helps address cross-device UI consistency. |
| CRN-2         |                      |                       | No relevant decisions made.                                            |
|               |              |           CRN-3              | Service-based architecture and Spring Framework support modularity. |
| CRN-4         |                      |                       | No relevant decisions made.                                            |
