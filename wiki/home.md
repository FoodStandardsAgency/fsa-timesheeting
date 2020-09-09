This wiki contains documentation describing the Meat Plant Inspection Timesheeting Service. It is intended to be a place where the squad (team) can keep track of progress and document their findings from the discovery, and extend into the full lifecycle of the service if it progresses to Alpha (and beyond). It is also intended to be a 'homepage' where the squad can signpost to data and information that exists elsewhere.
 
# Service

The timesheeting service exists to help the FSA pay for and recover costs of inspection duties carried out at meat plants.

It has evolved to support the payment and recharge of inspection services that the FSA has to undertake at food business operators, using staff and contract inspectors, vets and auditors.

[Read more...](service-overview)

# Users

Timesheeting service users fall into three main categories: 
1. Users who enter and submit timesheet (Field Staff)
2. Users who check and approve timesheets (Managers)
3. Users who use timesheet data entered (Backoffice)

Backoffice users are diverse and have different service goals, including paying staff, managing contractor payments, invoicing food business owners, recovering payments, and supporting field operations. 


[Read more...](/user-segments)

# Operations

The FSA are responsible for inspection control activity across 900 Food Business Operators in England and Wales. This is carried out by 450 staff and casuals, as well as 350 contractors supplied by Eville & Jones, currently the sole Service Delivery Partner.

Inspection control activity is expected to be recorded by Field Ops workers daily using the Timesheeting system.  Inspection Team Leaders verify submitted timesheets weekly, and any collected data is used in 4-5 week payroll and invoice runs that ensure staff and contractors are accurately paid, and that food business operators are accurately charged. 

Timesheeting is [governed](/governance-overview) by EU and UK legislation, and operated in line with HM Treasury and FSA policy.

[Read more...](/operational-overview)


# Technology

The timesheeting service uses a core bespoke Timesheeting application for both data entry and timesheet checking. Users typically access teh Microsoft Azure-hosted application via Digital Workplace on FSA managed devices (DellWyse terminals) within meat plants. Once logged in, permitted functionality is controlled through a separate system (TSAR), based on user role and plant (for activity logging). 

[Read more...](/technology-overview)

# Data

Data captured through the Timesheeting application is ultimately stored in the Single Information Repository (SIR) where it is then used for payroll, contractor payments and invoicing of food business operators. 

Reference data used directly by the Timesheeting system includes plant details (entered via the Establishments & People system). Other data sources are used as part of manual processes that sit around the timesheeting service, including for staff contract rates, worker rotas and resource allocation agreements (Statements of Resources). 

[Read more...](/data-assets)

# Recommendations

The main themes in our findings - which reinforce previous research projects - are that:
- Connectivity and system access slow down entering and reviewing timesheets
- Users need to manually cross-check against a number of data sources (eg, SOR, rota, IHR)
- Errors are easy to make, and the system doesn’t give users helpful or timely feedback
- Existing technology is not designed to meet modern standards

There is a recurring question about whether timesheeting is even necessary. The reality is the current legislation makes it unavoidable. Changing the business model of inspections charging that might eliminate it is a long term endeavour. In the meantime there are very practical and manageable steps that can be taken to make it a more efficient and effective service.

For any subsequent prototyping or Alpha phase, there are two key areas to test against to begin that service transformation process:

1. **Prototype user experience improvements** for pivotal user journey stages:
   - timesheet entry
   - comparing rota vs hours worked
   - user notifications
   - SOR reconciliation
1. **Investigate remote access options** for:
   - mobile user experience with offline sync
   - balancing security and remote access performance issues


[Read more...](/recommendations)