# Defect Lifecycle

## 1. Purpose

## 2. Defect States

## 3. Defect Workflow

## 4. Severity Levels

## 5. Priority Levels

## 6. Reopening Criteria

## 7. Closure Criteria

## 8. Example Defect Flow

### Scenario A: Successful Resolution (Happy Path)
1. **New:** A tester finds a broken button on the checkout page and logs the bug.
2. **Triaged:** The QA Lead and Product Manager review it and assign it to a sprint.
3. **In Progress:** A developer picks up the ticket and fixes the underlying code.
4. **Ready for Test:** The developer deploys the fix to the staging environment.
5. **Verified:** QA runs regression tests on the checkout page and confirms it works perfectly.
6. **Closed:** The bug is permanently closed and archived.

### Scenario B: Failed Validation (The Return Loop)
1. **Ready for Test:** The developer marks a login page bug as fixed.
2. **Reopened:** QA tests the login page, but the bug still happens on mobile screens. The tester changes the status to **Reopened** and adds a comment with new screenshots.
3. **In Progress:** The developer receives the notification, reviews the new mobile-specific data, and goes back to working on the code fix.