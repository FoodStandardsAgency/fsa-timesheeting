This page details opportunities indicated by the Timesheeting work that reach wider than the timesheeting system. They are noted here for reference and consideration.

## SIR Transformation

Updating the timesheet system provides an opportunity to review the SIR database and look at options for deeper back-end transformation. 

Whilst the body of this would need to sit outside the scope of Timesheeting, the approach to implementing changes to timesheeting can inform future direction and provide a starting point for SIR transformation.

The design of SIR contans a risk, often referred to as "[blast radius](https://www.ibm.com/garage/method/practices/manage/practice_limited_blast_radius/)". The term is used to describe the breadth of impact that failure of a single component would have on operations (e.g. the 2017 [Amazon s3 Service Disruption](https://aws.amazon.com/message/41926/)). In the case of SIR, a failure of the SQL database, the virtual machine hosting that database, or the virtual machine hosting the applications that rely on the database would lead to loss of service across the portfolio of applications that rely on tables in SIR.

Where the timesheeting could specifically contribute to wider SIR transformation options would be by demonstrating a transitional model, for example:
 * a new version of the application;
 * built separately from SIR;
 * within the food.gov domain;
 * designed to meet modern architecture and operational principles; and
 * enabling existing SIR processes to continue uninterrupted.

## FSA in-house technology capability

FSA currently supports systems and applications in-house, but contracts in external suppliers for development and maintenance of FSA-owned systems.

A number of FSA systems are supplied on a Software-as-a-Service basis, meaning that contract management and, where necessary, staff support are sufficient for ongoing operations. In-house technology capability is not directly required in these cases.

However FSA also operates a number of business-specific systems and applications, for example in the area of timesheeting. There is a consensus that these are aging and, whilst they are cloud-hosted and supported by an external supplier, there is limited capacity to readily iterate and improve them.

As a result it appears that these systems have fallen behind relative to industry standards and government digital recommendations, particularly in terms of accessibility, and there is a general acceptance that they need to be replaced.

Whilst there are low-code and software as a service options that could potentially be used to meet these needs, these nevertheless come with their own range of benefits and drawbacks. It may therefore be that this is a natural point to review the current model and consider whether developing a level of in-house FSA Digital Development capability would be advantageous.

FSA has coverage in terms of understanding the FSA context, pain points and opportunities from a number of individuals across the business, and has hands-on development capability at the database/SQL level, which has been effective in evolving and maintaining systems where this can be achieved via SQL jobs and stored procedures.

However, FSA does not currently maintain a full-stack hands-on technology team to curate a roadmap and implement system changes at other layers of the architecture. Timesheeting could provide a catalyst to rebalance the existing in-house technology capability and take ownership of architecture.

Such a capability could provide the following benefits:

 * Bring together hands-on knowledge and understandnig of the FSA context and the pain points and opportunities in the technology estate under a single team
 * A permanently-staffed ability to develop, iterate and maintain FSA-specific applications, systems and integraions in a range of architecture areas.
 * Ensure FSA systems continue to meet government digital standards and track evolving industry practice
 * Build a full-stack Technology capability to complement existing Digital and Data colleagues

Adding hands-on practical tech skills to the Digital team could increase self sufficiency and reduce reliance on external technology suppliers for maintenance and development beyond database/SQL. This would strengthen the ability of FSA to integrate with the government technology community and respond to evolving organisational needs and ongoing technology change.
