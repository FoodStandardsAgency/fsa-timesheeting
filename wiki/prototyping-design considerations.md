## Understand prototype design considerations

In the prototyping phase, we want to test hypotheses drawn from research completed in Discovery. As we design and iterate ideas, we need to take a range of business, process and technology constraints into account. These are not necessarily restrictions or blockers, but factors that must either be incorporated into the design or which help inform the direction we take.

### Activity Codes
- Activity codes are used to describe the type of work carried out at approved food establishments.
- Activity codes enable the FSA to split charges between the food business operator and government departments where it is performing activities on their behalf.
- Activity codes are used in conjunction with rate codes to adjust charges to industry/government and payment of inspection staff for premium services and work outside agreed hours.
- The current timesheeting application requires users to select an activity for each site within each plant that they work. They select a rate and enter the total number of hours spent completing that activity. The activity selected may require them to enter a free text comment to provide context.


For more information: https://docs.google.com/document/d/1GE0qNB8nboJrVw0qyGGDh20-Am93jT9n7n1-zmefYqk/edit#

# Prototype Design Handbook
**November 2019**
## Overview
This document outlines the process and resulting design decisions made during the prototyping stage. It includes the thinking behind certain elements and how they could be work. The recommendations contained in this outline are the result of several rounds of prototyping, feedback and iteration. They should be considered as a starting point for the next stages of development (clickable prototypes/alpha/beta) and may benefit from A/B testing at these stages.

[**Prototype walkthrough**](https://docs.google.com/presentation/d/1SabTDWI78DRQlKWlb6EMn03YZ1tgdwCw76NTexphaHE/edit#slide=id.g707b2e0d14_3_29)
## Goals
During the first week of the prototyping phase we identified the key areas/tasks that users carried out in the timesheeting system.
- “Saving minutes and seconds”

## Weekly Overview
### Week 1/2
- Met with digital user group and laid out the plan of approach to the coming weeks’ prototyping.
- Identified the areas of interest for this phase of the project
- Developed ideas for how the user flow could work.
### Week 2
- Started sketching the initial paper prototypes. These prototypes would cover the activity/breaks entry.
We came up with two initial approaches:
- A more, iterative change to the current process that would add one task at a time but one one screen (rather than the pop-ups that are found in the current system) - this approach received mixed feelings.
- The second was more of a departure from the current system introducing a checkbox view that reduced the need to change views down to two screens. This option has the potential to vastly improve the speed of entry for users day-to-day. It would also lend itself well to SOR and Rota integration, moving towards “entry by exception” in the future.
- This option was well received by all groups and was the idea that was pursued during this phase.
- Started to put screens in front of users including ITLs and Inspectors to gather feedback and iterate design.
### Week 3
- Designed the homepage overview screens and ideas for notification of missing/incorrect timesheets.
- Incorporation of feedback gained from users. Feedback included:
- The removing of start and end times of breaks
- Adding hours worked text box to the activity selections
- Further feedback sessions with ITLs, Inspectors and the finance team.
- Iterations based on these sessions.
- Giving teams the score cards to give us feedback
### Week 4
- Designed and presented an approach for dealing with notifications within the overview screen and how annual leave and sickness absence could work in the system when completing a timesheet.
- Gathered final feedback summary from all service users on the full journey. Including an in person walk-through of the prototypes
- The prototype design was very positively received.

## Design Elements
### Combo box
In most cases, any dropdown menus that appear in the prototypes will be some form of combo box. That is, a dropdown combined with a text box. Upon typing the items in the list will be filtered. This can be seen in [example 3 on W3.org](https://www.w3.org/TR/wai-aria-practices/examples/combobox/aria1.1pattern/listbox-combo.html#ex3_label):
![combo_box_example_1.png](/design/combo_box_example_1.png)
![combo_box_example_msdn.png](/design/combo_box_example_msdn.png)

The rationale behind the combo box is that while some users know the codes and some know the activity/site name it can be confusing particularly if searching for an item that they do not use very often. A combo box allows for quick typing in of a code/name if the user knows and all the available options if they do not.
In the context of timesheeting we have identified several situations where we think this element could work:
- Rate activity should be billed at - search by code and/or name
- Adding a new activity - Search by activity code (G/N etc codes) and/or activity name
- Plants - Search by plant code and/or name
- Sites - Search by site code and/or name

With all of these situations the items in the list will be only items relevant to the user. E.g. a contractor will only ever see one rate (00), the list of sites will only be those at the plant and available for the user’s role type. Activities will be dependant on user role - e.g. a OV vet will be presented with different options to a line inspector.
#### Defaults
On the plant combo box, the default option will be the user’s base plant. This can be taken from the database.
For the site combo box this will default to a Red Meat Slaughter House if one is available.
#### Notes and further reading
It is worth noting that the Government Digital Service Guidelines recommend using select boxes sparingly and that this combo-box would need to be a custom widget.
#### Further examples:
- [Microsoft Developer Docs - Drop-down Lists & Combo Boxes](https://docs.microsoft.com/en-us/windows/win32/uxguide/ctrl-drop)
- [Alice Bartlett: Burn your select tags](https://www.youtube.com/watch?v=CUkMCQR4TpY) - GDS talk on Select elements [including summary of custom widgets](https://youtu.be/CUkMCQR4TpY?t=1283)
### Standardised comments | Select/dropdown boxes
Subject to user acceptance testing due to GDS research showing users may not know how to use ([see Alice Bartlett video mentioned above](https://www.youtube.com/watch?v=CUkMCQR4TpY)). However, the select boxes could be used in situations where a comment needs to be added. It is envisaged that we can standardise regularly used comments. For example, there are around 12 standard reasons in the system handbook [LINK REQUIRED] as to why the N code “NOTH” should be used. At the moment users must type the reason into a text box. This has resulted in many variations of the same reason. 

This is the same with a user entering a reason for no break being taken:
![select_dropdown_1.jpg](/design/select_dropdown_1.jpg)

We believe that we can use a combination of database records and the reasons in the handbook to populate a dropdown menu with these standard comments - saving the user time and making data analysis and cleaning more efficient. Where comments are concerned we should always offer the user an “Other” option, that will display a free text entry box.
### Checkboxes
We propose that checkboxes be used to select daily activities and whether or not breaks were taken. This should work well on a mobile device - considerations should be made when sizing these to make it easy for users to click the box. Additionally, we suggest that the entire row be clickable. In the case of adding an activity, should the user begin typing into the text input, the check box should automatically get selected:
![checkbox_1.jpg](/design/checkbox_1.jpg)

In this example, clicking on the activity name would also select the checkbox.
