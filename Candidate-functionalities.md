## Two Candidate Major Functionalities
The proposed food marketplace system will support the management of food-quality and safety incidents through two interconnected major functionalities: 
1. Food Quality Incident Management.
2. Customer Traceability and Notification.

These functionalities address different stages of the incident management process. The first focuses on identifying, investigating and resolving potential food-quality concerns, while the second focuses on identifying and communicating with customers who may have purchased affected products.

### Functionality 1 Food Quality Incident Management
The Food Quality Incident Management functionality will provide a structured process for reporting, investigating, assessing and resolving potential food-quality or safety incidents within the marketplace.

Incidents may be reported by customers, producers or marketplace administrators and could include undeclared allergens, incorrect best-before dates, contamination or other concerns regarding product quality.

The functionality will allow marketplace representatives to manage incidents from their initial reporting through to their final resolution, ensuring that relevant information and decisions are recorded throughout the process.

**Key stakeholders**

- **Customers:** Report suspected food-quality or safety issues relating to purchased products.
- **Producers:** Report issues and provide additional information during investigations.
- **Marketplace administrators:** Register incidents, identify affected products and coordinate investigations.
- **Authorised marketplace representatives:** Assess the severity of incidents, approve necessary actions and determine whether incidents can be closed.

**Key business processes**

1. **Incident reporting and registration:** A customer, producer or administrator reports a suspected issue. An incident record is created containing the affected product, description of the issue, reporting date and current status.

2. **Product and producer identification:** The marketplace retrieves the relevant product and producer information to establish responsibility and support further investigation.

3. **Producer investigation:** The responsible producer is contacted and asked to provide information about the potential issue. Their response is recorded against the incident.

4. **Risk assessment:** An authorised marketplace representative evaluates the available evidence to determine whether the incident presents a genuine risk to customers.

5. **Product suspension:** Where appropriate, products associated with confirmed risks can be temporarily suspended from sale to prevent further purchases.

6. **Incident review and resolution:** Following the completion of required actions, an authorised representative reviews the incident and either closes it or requests further investigation.


The functionality will include incident creation, product identification, producer information retrieval, investigation tracking, risk assessment, product suspension and incident closure.

It will also maintain a history of incident statuses and decisions to provide traceability and accountability.

The functionality will not independently conduct physical food testing or determine whether a product is scientifically safe. Such decisions depend on information provided by producers and authorised marketplace representatives.

**Core data records**

- **Incident:** Unique identifier, reported issue, affected product, reporting date, reporter and incident status.
- **Product:** Product identifier, name, producer, availability status and relevant product information.
- **Producer:** Producer identifier, business name and contact details.
- **Investigation:** Associated incident, producer response, supporting information and investigation status.
- **Risk assessment:** Assessment outcome, severity, responsible representative and decision date.
- **Status history:** Record of actions, status changes, responsible users and timestamps.

This functionality will establish a consistent and traceable approach to food-quality incident management. It will support faster investigations, clearer organisational responsibilities and more reliable decision-making while reducing the likelihood of unresolved incidents or affected products remaining available for sale.

### Functionality 2 Customer Traceability and Notification
The Customer Traceability and Notification functionality will enable the marketplace to identify customers who have purchased products associated with confirmed food-quality or safety incidents and communicate relevant information to them.

Accurate traceability is essential because affected products may have been purchased by multiple customers across different orders. The system must therefore maintain relationships between products, producers, customer accounts and order records.

Once an incident requires customer communication, the functionality will identify the relevant customers, generate appropriate notifications and record the outcome of each communication attempt.

Failed notifications will be identified so that alternative communication methods or manual follow-up can take place.

**Key stakeholders**

- **Customers:** Receive information regarding affected products they have purchased and any recommended actions.
- **Marketplace administrators:** Identify affected orders, initiate notifications and monitor communication outcomes.
- **Producers:** Supply relevant product and incident information to support accurate customer communication.
- **Authorised marketplace representatives:** Verify that required notifications and follow-up actions have been completed before approving incident closure.

**Key business processes**

1. **Affected product identification:** Following an incident assessment, the system receives the identifier of the product associated with the food-quality concern.

2. **Order traceability:** The marketplace searches historical order records to identify all orders containing the affected product.

3. **Customer identification:** Customer records associated with the identified orders are retrieved, including the contact information required for communication.

4. **Notification preparation:** An appropriate notification is prepared containing information about the affected product, the identified concern and any actions customers should take.

5. **Customer notification:** The marketplace sends notifications to the identified customers through an appropriate communication channel, such as email.

6. **Delivery outcome recording:** Each notification attempt is recorded, including its status, timestamp and associated customer and incident.

7. **Failed notification handling:** Failed communication attempts are identified and flagged for retry, alternative communication or manual follow-up.

8. **Completion verification:** Marketplace representatives review notification outcomes and outstanding follow-up actions before confirming that the communication process is complete.

The functionality will include searching order records, identifying affected customers, preparing and sending notifications, recording communication outcomes and managing failed notification attempts.

It will maintain traceability between customers, orders, products, producers and incidents to support accurate identification of affected individuals.

The functionality will not manage physical product recalls, organise the return of affected products or process financial compensation. These activities are outside the proposed scope, although they could be considered for future development.

**Core data records**

- **Order:** Unique order identifier, customer, purchase date and order status.
- **Order item:** Relationship between an order and its purchased products, including product identifiers and quantities.
- **Customer:** Customer identifier, name and relevant contact information.
- **Notification:** Associated incident, customer, communication content, selected channel and current status.
- **Notification attempt:** Individual delivery attempt, timestamp, outcome and any recorded failure information.
- **Follow-up action:** Required alternative communication, assigned representative and completion status.

This functionality will improve the marketplace's ability to identify and contact customers affected by food-quality incidents.

By automating the identification of relevant orders and recording communication outcomes, the system will reduce reliance on manual searches and provide greater visibility over which customers have been contacted successfully.

The functionality will also support incident accountability by ensuring that unsuccessful notifications are identified and addressed rather than being overlooked.

### Relationship Between the Two Functionalities

Although the two functionalities address different business responsibilities, they are closely connected.

Food Quality Incident Management is responsible for establishing the nature of an incident, investigating the potential risk and determining which actions are necessary.

Customer Traceability and Notification supports the response to incidents requiring customer communication by identifying affected purchasers and managing notification outcomes.

For example, when a marketplace representative confirms that a product contains an undeclared allergen, the incident management functionality can initiate the appropriate response, including product suspension where necessary.

The customer traceability functionality can then identify orders containing the affected product and initiate notifications to the relevant customers.

Notification outcomes and outstanding follow-up actions can subsequently be made available to the incident management process, allowing an authorised representative to determine whether the incident is ready for closure.

This separation of responsibilities supports a modular system design while maintaining a coordinated end-to-end incident management process.
