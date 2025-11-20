Step 2: Establish Iteration Goal
The goal of this iteration is to identify and define sructures that directly support the primary use cases, and these include:
UC-1
CRN-1
CON-1
CON-3

Step 3: Choose Elements of the System to Refine
In this iteration we will focus on refining the core structural elements needed to establish the basic structure for AIDAP.

Step 4: Choosing Design Concepts that satisfy the selected drivers
1. Refining the Rich Internet Application (RIA) Frontend:
   We want to continue to refine the RIA mentioned in iteration 1 by primarily focusing on how the RIA supports the specific primary workflows:
   For UC-1 (sign in), UC-2(monitoring), and UC-3(user management), the RIA will provide:
   - Responsive input validation
   - Dynamic component updates using AJAX
   - Accessibility hooks for screen readers (CON-3)
   - Consistent multi-device behaviour (CON-1)
In this stage of the process, we begin defining the UI components that will be required later, such as the login interface, monitoring dashoard layouts, and administrative panels and these will support CON-1, CON-2, and CRN-1
2. Refining the Service-Based Application Backend:
   In this iteration we want to extend the service-backend concept by assigning clear responsibilities to services that directly support our three use cases which include:
   - Authentication-Service (UC-1)
   - Metrics Service (UC-2)
   - User-Admin-Service (UC-3)
  This will ensure that the backend remains modular and secure by separating UI logic from sensitive operations like account verification, metrics processing and user role administration and these will support UC-1, UC-3, CRN-3, QA-1)

3. Applying the Four-Tier Deployment Structure to Use Cases:
   In iteration 1, we had a four-tier structure that we want to apply to the workkflow behaviour for this iteration:
   - The client tier will handle dynamic UI interations
   - The API tier will route sign-in, monitoring, and admin requests
   - The application logic tier wil perform validation, audiiting, and role checks
   - The database tier will store users, metris, sessions and also bugs
In implementing this, we believe that it will ensure isiolation between public UI requests and sensitive backend operations, which is critical for system maintainers monitoring uptime (UC-2), and administrators modifying users (UC-3). These wil support QA-2, QA-1, and CON-4

4. Using the Spring Frameword for Module Definition
   So we selected Spring as the core framework that we'll use in Iteration 1, and we intend to refine its application more in Iteration 2:
   - Spring Security defines authentication flows (UC-1)
   - Spring Boot services will formalize metrics retrieval (UC-2)
   - Dependency injection will simplify controller/service wiring (UC-3)
   - Spring’s modular structure will prepare AIDAP for future AI extensions
This deepens the maintainability and scalability benefits originally identified and will support CRN-3, QA-4, CON-4 and UC-1.
   

STEP 5:

1: Create a dedicated autentication and role-management module
Supports SSO, traceability and role based UI. 
(UC-1, UC-3, QA-1)

2: Create a operational monitoring module
Supports a dashboard populated with metrics and the status of the various parts of the application.
(UC-2)

3: Create a personalization module
Stores user preferences regarding language, conversation style, UI mode and notification settings
(UC-4, QA-5)
