# Test Execution Report

## Project Name
Police Duty Management System

## Execution Summary Table

| TC ID | Module | Scenario ID | Status | Remarks |
|------|--------|-------------|--------|---------|
| TC-AUTH-001 | Authentication | TS-AUTH-001 | Passed | Login working as expected |
| TC-AUTH-002 | Authentication | TS-AUTH-002 | Passed | Invalid login handled correctly |
| TC-USER-001 | User Management | TS-USER-001 | Passed | User creation successful |
| TC-USER-003 | User Management | TS-USER-003 | Passed | Duplicate user blocked |
| TC-RBAC-001 | RBAC | TS-RBAC-001 | Passed | Full access verified |
| TC-DUTY-001 | Duty Management | TS-DUTY-001 | Passed | Duty created successfully |
| TC-DUTY-004 | Duty Management | TS-DUTY-004 | Passed | Duty assigned correctly |
| TC-NOTIF-001 | Notification | TS-NOTIF-001 | Passed | Notification delivered |
| TC-TRACK-001 | Live Tracking | TS-TRACK-001 | Passed | Live location updated |
| TC-TRACK-007 | Live Tracking | TS-TRACK-007 | Failed | Geo-fence alert delayed |


## Execution Summary

- Total Test Cases: 50+
- Passed: 49
- Failed: 1
- Pass Rate: 98%


## Failed Test Cases

| TC ID | Bug ID | Reason |
|------|--------|--------|
| TC-TRACK-007 | BUG-005 | Geo-fencing alert delay observed |