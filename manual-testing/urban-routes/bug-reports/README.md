# Car Sharing cancellation modal does not close when clicking "x" during free waiting time

## Environment
- Browser: Google Chrome / Firefox
- Resolution: 800x600, 1920x1080
Priority High
Severity: Major

---

## Description
When attempting to cancel a Car Sharing ride during the free waiting time by clicking the “X” button in the “Car Reserved” modal, the modal does not close as expected.

---

## Preconditions
- User on the route planning page

---

## Steps to Reproduce
1. Go to the test environment
2. Enter **"1917 Bay St"** in the From field
3. Enter **"615 S Broadway"** in the To field
4. Select **Personal** mode
5. Choose **Car Sharing** as Transport type
6. Click **Reserve**
7. Click the **"X"** button before the free waiting time expires

---

## Expected Result
The "Car Reserved" modal should close and the ride should be canceled without additional actions.

---

## Actual Result
Clicking the "X" botton does not close the modal and the ride remains active

---

## Notes
Issue reproduced on multiple browsers and screen resolutions
