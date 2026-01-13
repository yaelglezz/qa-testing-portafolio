# UI Design Checklist – Urban Routes

## Overview
This checklist was created to validate the UI design and functional behavior of the Urban Routes web application, focusing on the Shared Car reservation flow. The validations are based on the design specifications and functional requirements provided for the project.

The checklist covers layout consistency, form behavior, map interaction, travel options, vehicle selection, and reservation confirmation elements. It was executed through manual testing in multiple browsers, and any deviations from the expected behavior were reported and tracked in Jira.

## Layout

- The **Urban Routes** logo is displayed in the top-left corner
- The map is displayed on the right side of the application
- The **“Reserve”** button is located in the bottom-left corner of the screen

## Address Fields

- The **“From”** field is empty by default
- The **“From”** placeholder is displayed correctly when the field is empty
- When typing in the **“From”** field, the label remains visible and the user input is displayed correctly
- The **“To”** field is empty by default
- The **“To”** placeholder is displayed correctly when the field is empty
- When typing in the **“To”** field, the label remains visible and the user input is displayed correctly

## Map and Route

- When valid addresses are entered in the **“From”** and **“To”** fields, a route is generated on the map
- The route displays a starting pin (**A**)
- The route displays a destination pin (**B**)
- The route is displayed in blue
- The map automatically zooms to fit the generated route

## Travel Options

- Travel options are enabled once a valid route is generated
- The **“Flash”** option is selected by default
- The selected option is highlighted with a gray indicator
- The text of the selected option changes to white
- The **“Optimal”**, **“Flash”**, and **“Personal”** options do not contain spelling errors

## Transportation Types

- The **Car** option is displayed
- The **Walking** option is displayed
- The **Taxi** option is displayed
- The **Bicycle** option is displayed
- The **Scooter** option is displayed
- The **Shared Car** option is displayed

## Trip Information

- The exact trip price is displayed correctly
- The estimated trip duration is displayed correctly
- Price information, trip duration, and the **“Reserve”** button are displayed below the travel modes
- When clicking the **“Reserve”** button, the order form is displayed

## Reservation Form

- The form matches the specified design
- The form does not contain spelling errors
- The **“Casual”** fare is selected by default
- The selected fare is highlighted in gray
- The **“Add driver’s license”** field is empty by default
- The **“Payment method”** field is empty by default
- If no bank card is added, the **“Add”** option is displayed instead of **“Card”**

## Vehicle Selection

- Vehicle images are displayed correctly for each fare
- The **“Casual”** option displays the correct label
- The **“Camping”** option displays the correct label
- The **“Luxury”** option displays the correct label
- The nearest vehicle is highlighted with a larger icon on the map
- The nearest vehicle displays a black label with the vehicle brand
- Non-selected vehicles remain visible on the map
- When selecting a vehicle, its icon becomes larger
- When selecting a vehicle, a black label with the vehicle brand is displayed
- The selected vehicle information is updated in the left panel

## Reservation Confirmation

- The **“Car Reserved”** modal is displayed
- The modal displays:
  - Vehicle brand
  - License plate number
  - Vehicle icon
  - Vehicle location
  - Trip price
  - Free waiting time countdown
  - The **"X"** button to cancel is at the top center
 
---

## Test Execution Notes

The checklist was executed on the following environments:
- Google Chrome
- Mozilla Firefox

Some checklist items did not pass due to deviations from the specified UI and functional requirements. All failed validations were documented and reported as bugs in Jira to ensure proper tracking and follow-up.



