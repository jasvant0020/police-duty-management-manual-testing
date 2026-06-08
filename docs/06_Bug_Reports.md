# Bug Reports

| Bug ID | Module | Title | Steps to Reproduce | Expected Result | Actual Result | Severity | Priority | Status |
|--------|--------|-------|-------------------|-----------------|--------------|----------|----------|--------|
| BUG-001 | Authentication | Login fails with valid credentials intermittently | 1. Enter valid username 2. Enter valid password 3. Click login | User should login successfully | Sometimes login fails without error | High | High | Open |
| BUG-002 | User Management | Duplicate user allowed | 1. Create user with same username twice | System should prevent duplicate user | Duplicate user is created | High | High | Open |
| BUG-003 | Duty Management | Duty not assigned to selected staff | 1. Assign duty 2. Select staff 3. Save | Duty should be assigned | Duty remains unassigned | Critical | High | Open |
| BUG-004 | Notification | Notification not delivered in real-time | 1. Send notification 2. Observe recipient | Notification should appear instantly | Delay observed in delivery | Medium | Medium | Open |
| BUG-005 | Live Tracking | Location not updating on map | 1. Move user location 2. Check map | Map should update live location | Location remains static | High | High | Open |
