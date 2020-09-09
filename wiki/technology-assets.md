
Asset name       | Description                        | Supplier / Vendor      | Infrastructure  | Notes
---------------- | ---------------------------------- | ---------------------- | --------------- | ----------------------
Timesheet system | Time entry, checking and approvals | FSA IT / Civica        | Azure vm/sql (part of SIR) | 12 year-old application. Functional but time-consuming and error-prone.
Timesheet Access Register (TSAR) | Identity and access management for Timesheets | Civica        | Azure vm/sql (part of SIR)    | Similar age to Timesheets system, but implemented more recently. Additionally provides filtering of activity codes that are displayed to users. 
Establishments and People | details of people who use timesheets | n/a | Azure vm/sql (part of SIR) | Contractors are manually entered into EnP and staff are automatically synchronised from iTrent.
Finance system   | FSA finance system (SOP)           | Oracle            | Gov shared service | Self-billing to pay contractors. Overtime payments for employed staff. Invoicing FBOs.
iTrent           | FSA HR system | Midland | Hosted service | Source for timesheeting of FSA employees who do meat plant inspections. Destination for Casual Payroll and Overtime Charging data.
Smartphones      | FSA Staff have Android phones      | Samsung           | Samsung J5, Android 7/8 | Contract staff are required to have a smartphone, so all front-line staff will have a smartphone
