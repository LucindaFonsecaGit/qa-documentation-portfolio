# Test Plan: E-Commerce Web Application

**Document Version:** 2.1  
**Status:** Approved  
**Author:** Lucinda Fonseca  
**Date:** 2024-04-01  
**Project:** ShopNow E-Commerce Platform — v3.2 Release  

---

## 1. Introduction

### 1.1 Purpose

This test plan defines the testing approach, scope, resources, and schedule for the ShopNow e-commerce platform v3.2 release. It covers all testing activities from test design through to sign-off.

### 1.2 Project Overview

ShopNow is a B2C e-commerce web application serving 50,000+ active users. Version 3.2 introduces a new checkout flow, discount code functionality, wishlist feature, and updates to the REST API.

---

## 2. Test Objectives

1. Verify all new features function as specified in the requirements
2. Confirm no regression defects were introduced in existing functionality
3. Validate API security — all endpoints correctly enforce authentication
4. Confirm the application is usable on Chrome, Firefox, Safari, and mobile browsers
5. Ensure checkout flow handles edge cases (expired cards, insufficient stock, etc.)

---

## 3. Scope

### 3.1 In Scope

- User registration and authentication (including password reset)
- Product search and filtering
- Shopping cart (add, update, remove)
- New checkout flow (v3.2)
- Discount codes (new feature)
- Wishlist (new feature)
- REST API endpoints (authentication, users, products, orders)
- Cross-browser testing: Chrome, Firefox, Safari, Edge
- Mobile responsive testing: iOS Safari, Android Chrome

### 3.2 Out of Scope

- Payment gateway infrastructure testing
- Performance/load testing (separate engagement)
- Accessibility testing (planned for v3.3)
- Back-office admin panel
- Email delivery infrastructure

---

## 4. Test Types

### 4.1 Functional Testing
Verify that each feature works as specified. Priority given to critical paths: registration, login, add-to-cart, checkout.

### 4.2 Negative Testing
Validate system behaviour with invalid, unexpected, or boundary inputs. Ensure helpful error messages are displayed and no crashes occur.

### 4.3 Regression Testing
Run the full regression test suite after each build to confirm existing features are unaffected by new changes.

### 4.4 Security Testing
Verify that:
- All API endpoints require valid authentication tokens
- Session tokens expire correctly
- Password reset links are single-use and time-limited
- No sensitive data exposed in API responses

### 4.5 Cross-Browser / Cross-Device Testing
Manually verify key user journeys on all in-scope browsers and devices.

### 4.6 API Testing
Test REST API endpoints using Postman. Validate: response codes, response body schema, authentication enforcement, error handling.

---

## 5. Entry Criteria

- [ ] Build deployed to staging environment
- [ ] Smoke test passed (core navigation functional)
- [ ] Test data seeded in staging database
- [ ] Test cases reviewed and approved
- [ ] All critical-priority stories from sprint marked as development complete

## 6. Exit Criteria

- [ ] All planned test cases executed
- [ ] Zero open P1 (Critical) defects
- [ ] Zero open P2 (High) defects
- [ ] P3/P4 defects reviewed and accepted by Product Owner
- [ ] Regression suite pass rate ≥ 98%
- [ ] Sign-off received from QA Lead and Product Owner

---

## 7. Test Environment

| Environment | URL | Purpose |
|---|---|---|
| Staging | https://staging.shopnow.example.com | Primary testing |
| UAT | https://uat.shopnow.example.com | Business sign-off |
| Production | https://www.shopnow.example.com | Post-release smoke test only |

**Test Data:** Seeded via setup scripts. Test payment cards provided by Stripe test environment.

---

## 8. Tools

| Tool | Purpose |
|---|---|
| Jira | Defect management, test management (Xray) |
| Confluence | Documentation |
| Postman | API testing |
| Playwright | Automated regression (smoke + regression suite) |
| BrowserStack | Cross-browser / cross-device testing |
| Slack | Team communication and defect escalation |

---

## 9. Roles and Responsibilities

| Role | Name | Responsibilities |
|---|---|---|
| QA Lead | Lucinda Fonseca | Test planning, test execution, defect management, reporting |
| Developer | B. Rodrigues | Defect investigation and fixes |
| Developer | T. Alves | Defect investigation and fixes |
| Product Owner | M. Santos | Requirements clarification, UAT sign-off |
| DevOps | J. Carvalho | Environment support, build deployments |

---

## 10. Defect Management

All defects logged in Jira with the following severity classification:

| Severity | Definition | Resolution SLA |
|---|---|---|
| Critical (P1) | Showstopper — blocks testing or causes data loss / security breach | Same day |
| High (P2) | Key feature broken or security vulnerability | 48 hours |
| Medium (P3) | Feature works but has significant issue | Next sprint |
| Low (P4) | Cosmetic, minor UX issue | Backlog |

---

## 11. Risk and Mitigation

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| Staging environment unstable | Medium | High | Daily smoke test; escalate to DevOps immediately |
| Late delivery of features | Medium | High | Agree feature freeze date; deprioritise lower-priority test cases |
| Test data corruption | Low | Medium | Daily test data refresh script |
| Browser-specific bug found late | Low | Medium | Run cross-browser checks from day 1 of cycle |

---

## 12. Schedule

| Phase | Duration | Dates |
|---|---|---|
| Test planning & design | 3 days | 2024-04-01 – 2024-04-03 |
| Test environment setup | 1 day | 2024-04-04 |
| Test execution – cycle 1 | 5 days | 2024-04-08 – 2024-04-12 |
| Defect retesting – cycle 1 | 2 days | 2024-04-15 – 2024-04-16 |
| Test execution – cycle 2 | 3 days | 2024-04-17 – 2024-04-19 |
| Regression run | 1 day | 2024-04-22 |
| UAT support | 2 days | 2024-04-23 – 2024-04-24 |
| Sign-off & release | 1 day | 2024-04-25 |

---

## 13. Approval

| Name | Role | Decision | Date |
|---|---|---|---|
| Lucinda Fonseca | QA Lead | ✅ Approved | 2024-04-01 |
| M. Santos | Product Owner | ✅ Approved | 2024-04-02 |
