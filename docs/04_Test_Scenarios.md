# Test Scenarios

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-AUTH-001 | Authentication | Login | Verify login with valid credentials |
| TS-AUTH-002 | Authentication | Login | Verify login with invalid username |
| TS-AUTH-003 | Authentication | Login | Verify login with invalid password |
| TS-AUTH-004 | Authentication | Login | Verify login with invalid username and password |
| TS-AUTH-005 | Authentication | Login | Verify login with empty username |
| TS-AUTH-006 | Authentication | Login | Verify login with empty password |
| TS-AUTH-007 | Authentication | Login | Verify login with both fields empty |
| TS-AUTH-008 | Authentication | Password | Verify password is masked |
| TS-AUTH-009 | Authentication | Logout | Verify user can logout successfully |
| TS-AUTH-010 | Authentication | Session | Verify session is terminated after logout |

## User Management

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-USER-001 | User Management | Create User | Verify admin can create a new user with valid data |
| TS-USER-002 | User Management | Create User | Verify system does not allow creating user with empty fields |
| TS-USER-003 | User Management | Create User | Verify system prevents duplicate username creation |
| TS-USER-004 | User Management | Edit User | Verify admin can update user details |
| TS-USER-005 | User Management | Edit User | Verify system validates updated email format |
| TS-USER-006 | User Management | Delete User | Verify admin can delete an existing user |
| TS-USER-007 | User Management | Delete User | Verify system asks confirmation before deletion |
| TS-USER-008 | User Management | Role Assignment | Verify admin can assign role to a user |

## Role-Based Access Control

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-RBAC-001 | RBAC | Login Access | Verify Master Admin can access all modules |
| TS-RBAC-002 | RBAC | Login Access | Verify Super Admin has restricted access compared to Master Admin |
| TS-RBAC-003 | RBAC | Login Access | Verify Admin cannot access Master Admin features |
| TS-RBAC-004 | RBAC | Login Access | Verify GD Munsi can only manage duty assignment features |
| TS-RBAC-005 | RBAC | Login Access | Verify Field Staff can only view assigned duties |
| TS-RBAC-006 | RBAC | Login Access | Verify VVIP can only view personal assigned security details |
| TS-RBAC-007 | RBAC | Permission | Verify unauthorized user cannot access restricted URL manually |
| TS-RBAC-008 | RBAC | Permission | Verify hidden menu items are not visible for restricted roles |
| TS-RBAC-009 | RBAC | Session | Verify role permissions persist after login session refresh |
| TS-RBAC-010 | RBAC | Security | Verify user cannot switch role by manipulating frontend data |


## Duty Management

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-DUTY-001 | Duty Management | Create Duty | Verify admin can create a new duty with valid details |
| TS-DUTY-002 | Duty Management | Create Duty | Verify system does not allow duty creation with empty fields |
| TS-DUTY-003 | Duty Management | Create Duty | Verify duty cannot be created with invalid location data |
| TS-DUTY-004 | Duty Management | Assign Duty | Verify GD Munsi can assign duty to field staff |
| TS-DUTY-005 | Duty Management | Assign Duty | Verify system prevents assigning same duty to multiple staff without permission |
| TS-DUTY-006 | Duty Management | Update Duty | Verify admin can update duty details |
| TS-DUTY-007 | Duty Management | Delete Duty | Verify admin can delete a duty only if not active |
| TS-DUTY-008 | Duty Management | Duty Status | Verify duty status updates correctly (Active / Completed / Cancelled) |
| TS-DUTY-009 | Duty Management | Validation | Verify duty cannot be assigned outside allowed time range |
| TS-DUTY-010 | Duty Management | Security | Verify unauthorized user cannot create or modify duties |


## Notification Management

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-NOTIF-001 | Notification | Send Notification | Verify user can send a normal notification successfully |
| TS-NOTIF-002 | Notification | Send Notification | Verify system does not send empty notifications |
| TS-NOTIF-003 | Notification | Broadcast | Verify admin can broadcast notification to all users |
| TS-NOTIF-004 | Notification | Role-Based | Verify notification is delivered only to selected role |
| TS-NOTIF-005 | Notification | SOS Alert | Verify SOS alert is triggered successfully |
| TS-NOTIF-006 | Notification | Real-Time | Verify notification appears instantly without page refresh |
| TS-NOTIF-007 | Notification | History | Verify notification history is stored correctly |
| TS-NOTIF-008 | Notification | Read Status | Verify notification read/unread status updates correctly |
| TS-NOTIF-009 | Notification | Security | Verify unauthorized user cannot send system-wide notifications |
| TS-NOTIF-010 | Notification | Delivery | Verify notification is received by correct recipient only |


## Live Tracking System

| Scenario ID | Module | Feature | Scenario Description |
|------------|----------|----------|----------|
| TS-TRACK-001 | Live Tracking | Staff Location | Verify staff location is updated in real-time |
| TS-TRACK-002 | Live Tracking | VVIP Tracking | Verify VVIP location is visible to authorized roles |
| TS-TRACK-003 | Live Tracking | Map View | Verify map loads correctly with all markers |
| TS-TRACK-004 | Live Tracking | Location Update | Verify location updates without page refresh |
| TS-TRACK-005 | Live Tracking | Accuracy | Verify location accuracy within allowed radius |
| TS-TRACK-006 | Live Tracking | Offline Handling | Verify system behavior when GPS signal is lost |
| TS-TRACK-007 | Live Tracking | Geo-Fencing | Verify alert is triggered when user leaves assigned area |
| TS-TRACK-008 | Live Tracking | Role Access | Verify only authorized roles can view tracking data |
| TS-TRACK-009 | Live Tracking | Performance | Verify map performance with multiple live users |
| TS-TRACK-010 | Live Tracking | Security | Verify tracking data cannot be accessed via unauthorized URL |