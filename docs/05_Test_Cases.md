# Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-AUTH-001 | TS-AUTH-001 | Authentication | Login with valid credentials | 1. Open login page 2. Enter valid username 3. Enter valid password 4. Click Login | User should login successfully and redirect to dashboard |
| TC-AUTH-002 | TS-AUTH-002 | Authentication | Login with invalid username | 1. Enter invalid username 2. Enter valid password 3. Click Login | System should show error message |
| TC-AUTH-003 | TS-AUTH-003 | Authentication | Login with invalid password | 1. Enter valid username 2. Enter invalid password 3. Click Login | System should reject login |
| TC-AUTH-004 | TS-AUTH-005 | Authentication | Login with empty username | 1. Leave username empty 2. Enter password 3. Click Login | Validation message should appear |
| TC-AUTH-005 | TS-AUTH-006 | Authentication | Login with empty password | 1. Enter username 2. Leave password empty 3. Click Login | Validation message should appear |
| TC-AUTH-006 | TS-AUTH-009 | Authentication | Logout functionality | 1. Login successfully 2. Click logout button | User should be logged out and redirected to login page |


## User Management Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-USER-001 | TS-USER-001 | User Management | Create user with valid data | 1. Login as Admin 2. Open User Management 3. Enter valid user details 4. Click Create | User should be created successfully |
| TC-USER-002 | TS-USER-002 | User Management | Create user with empty fields | 1. Leave all fields empty 2. Click Create | System should show validation errors |
| TC-USER-003 | TS-USER-003 | User Management | Prevent duplicate username | 1. Create user with existing username 2. Click Create | System should show duplicate error |
| TC-USER-004 | TS-USER-004 | User Management | Edit user details | 1. Select existing user 2. Update details 3. Save changes | User details should be updated successfully |
| TC-USER-005 | TS-USER-005 | User Management | Validate email format during edit | 1. Enter invalid email 2. Save changes | System should show email validation error |
| TC-USER-006 | TS-USER-006 | User Management | Delete user | 1. Select user 2. Click delete 3. Confirm deletion | User should be deleted successfully |
| TC-USER-007 | TS-USER-007 | User Management | Confirm before deletion | 1. Click delete user 2. Cancel confirmation | User should not be deleted |
| TC-USER-008 | TS-USER-008 | User Management | Assign role to user | 1. Select user 2. Assign role 3. Save | Role should be assigned successfully |


## Role-Based Access Control Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-RBAC-001 | TS-RBAC-001 | RBAC | Verify Master Admin access to all modules | 1. Login as Master Admin 2. Navigate all modules | Master Admin should access all features without restriction |
| TC-RBAC-002 | TS-RBAC-002 | RBAC | Verify Super Admin restricted access | 1. Login as Super Admin 2. Try accessing Master Admin panel | Access should be restricted |
| TC-RBAC-003 | TS-RBAC-003 | RBAC | Verify Admin cannot access Master Admin features | 1. Login as Admin 2. Try accessing restricted URLs | System should deny access |
| TC-RBAC-004 | TS-RBAC-004 | RBAC | Verify GD Munsi duty management access | 1. Login as GD Munsi 2. Access duty module | GD Munsi should access only duty module |
| TC-RBAC-005 | TS-RBAC-005 | RBAC | Verify Staff limited access | 1. Login as Staff 2. Try accessing admin features | Access should be restricted |
| TC-RBAC-006 | TS-RBAC-006 | RBAC | Verify VVIP view-only access | 1. Login as VVIP 2. Try editing data | Editing should not be allowed |
| TC-RBAC-007 | TS-RBAC-007 | RBAC | Verify direct URL access restriction | 1. Login as low role user 2. Paste admin URL manually | Access should be blocked |
| TC-RBAC-008 | TS-RBAC-008 | RBAC | Verify hidden menu visibility | 1. Login with different roles 2. Check UI menus | Only allowed menus should be visible |
| TC-RBAC-009 | TS-RBAC-009 | RBAC | Verify session role persistence | 1. Login 2. Refresh page | Role permissions should remain same |
| TC-RBAC-010 | TS-RBAC-010 | RBAC | Verify role tampering prevention | 1. Try modifying role in frontend storage 2. Refresh | System should not allow role change |


## Duty Management Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-DUTY-001 | TS-DUTY-001 | Duty Management | Create duty with valid details | 1. Login as Admin 2. Open Duty Module 3. Enter valid duty details 4. Click Create | Duty should be created successfully |
| TC-DUTY-002 | TS-DUTY-002 | Duty Management | Create duty with empty fields | 1. Leave fields empty 2. Click Create | System should show validation errors |
| TC-DUTY-003 | TS-DUTY-003 | Duty Management | Create duty with invalid location | 1. Enter invalid coordinates 2. Click Create | System should reject invalid location |
| TC-DUTY-004 | TS-DUTY-004 | Duty Management | Assign duty to staff | 1. Login as GD Munsi 2. Select duty 3. Assign staff | Duty should be assigned successfully |
| TC-DUTY-005 | TS-DUTY-005 | Duty Management | Prevent multiple assignment without permission | 1. Try assigning same duty to multiple staff | System should restrict multiple assignment |
| TC-DUTY-006 | TS-DUTY-006 | Duty Management | Update duty details | 1. Select duty 2. Edit details 3. Save | Duty should be updated successfully |
| TC-DUTY-007 | TS-DUTY-007 | Duty Management | Delete inactive duty | 1. Select inactive duty 2. Click delete | Duty should be deleted successfully |
| TC-DUTY-008 | TS-DUTY-008 | Duty Management | Duty status change | 1. Change status Active → Completed | Status should update correctly |
| TC-DUTY-009 | TS-DUTY-009 | Duty Management | Validate duty time range | 1. Enter invalid time range 2. Save | System should show error |
| TC-DUTY-010 | TS-DUTY-010 | Duty Management | Unauthorized duty access | 1. Login as Staff 2. Try editing duty | Access should be denied |


## Notification Management Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-NOTIF-001 | TS-NOTIF-001 | Notification | Send normal notification | 1. Login as Admin 2. Create notification 3. Send | Notification should be delivered successfully |
| TC-NOTIF-002 | TS-NOTIF-002 | Notification | Prevent empty notification | 1. Try sending empty message | System should show validation error |
| TC-NOTIF-003 | TS-NOTIF-003 | Notification | Broadcast notification | 1. Send broadcast message | All users should receive notification |
| TC-NOTIF-004 | TS-NOTIF-004 | Notification | Role-based delivery | 1. Send notification to specific role | Only selected role should receive it |
| TC-NOTIF-005 | TS-NOTIF-005 | Notification | SOS alert trigger | 1. Trigger SOS alert | Emergency notification should be sent |
| TC-NOTIF-006 | TS-NOTIF-006 | Notification | Real-time delivery | 1. Send notification 2. Observe UI | Notification should appear instantly |
| TC-NOTIF-007 | TS-NOTIF-007 | Notification | Notification history | 1. Send notifications 2. Check history | All notifications should be stored |
| TC-NOTIF-008 | TS-NOTIF-008 | Notification | Read/unread status | 1. Open notification 2. Mark as read | Status should update correctly |
| TC-NOTIF-009 | TS-NOTIF-009 | Notification | Unauthorized access | 1. Login as low role 2. Try sending system notification | Access should be denied |
| TC-NOTIF-010 | TS-NOTIF-010 | Notification | Correct recipient delivery | 1. Send targeted message | Only intended user should receive it |



## Live Tracking System Test Cases

| TC ID | Scenario ID | Module | Test Case Title | Steps | Expected Result |
|------|-------------|--------|----------------|------|-----------------|
| TC-TRACK-001 | TS-TRACK-001 | Live Tracking | Verify staff live location update | 1. Login as Staff 2. Move location 3. Observe map | Location should update in real-time |
| TC-TRACK-002 | TS-TRACK-002 | Live Tracking | Verify VVIP tracking visibility | 1. Login as Admin 2. View VVIP location | VVIP location should be visible only to authorized roles |
| TC-TRACK-003 | TS-TRACK-003 | Live Tracking | Verify map loading with markers | 1. Open tracking dashboard | Map should load with correct markers |
| TC-TRACK-004 | TS-TRACK-004 | Live Tracking | Verify real-time updates without refresh | 1. Change location 2. Do not refresh page | Updates should reflect automatically |
| TC-TRACK-005 | TS-TRACK-005 | Live Tracking | Verify location accuracy | 1. Compare actual vs displayed location | Location should be within allowed radius |
| TC-TRACK-006 | TS-TRACK-006 | Live Tracking | Verify GPS offline handling | 1. Turn off GPS 2. Observe system behavior | System should handle missing GPS gracefully |
| TC-TRACK-007 | TS-TRACK-007 | Live Tracking | Verify geo-fencing alert | 1. Move outside boundary | System should trigger alert |
| TC-TRACK-008 | TS-TRACK-008 | Live Tracking | Verify role-based access | 1. Login as unauthorized user | Access should be restricted |
| TC-TRACK-009 | TS-TRACK-009 | Live Tracking | Verify performance with multiple users | 1. Simulate multiple tracked users | System should remain responsive |
| TC-TRACK-010 | TS-TRACK-010 | Live Tracking | Verify tracking security | 1. Try accessing tracking via URL manipulation | Access should be blocked |



