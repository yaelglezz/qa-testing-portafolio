## Test Case ID
TC-SHARED-CAR-005
## Test Case Title
Cancel shared car reservation during free waiting time using the "X" button
## Preconditions
- User is on Urban Routes test environment
- Shared Car service is available
## Test Steps
1. Navigate to te test environment
2. Enter "1917 Bay St" in the **From** field
3. Enter "615 S Broadway" in the **To** field
4. Select **Personal** mode
5. Select **Shared Car** as transportation method
6. Click **Reserve**
7. While the free waiting time is active, click the **"X"** button
## Expected Result
The "Car Reserved" modal closes successfully and the user from canceling the reservation.
## Status
❌ Failed
## Priority
High
## Enviroment
- Browser: Google Chrome, Firefox
- Resolution: 800x600, 1920x1080
## Linked Bug
Bug reported in Jira: *Car Sharing cancellation modal does not close when clicking "x" during free waiting time*
