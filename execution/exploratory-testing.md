# Exploratory Testing

## 1. Purpose

## 2. When to Use Exploratory Testing

## 3. Session-Based Testing

## 4. Test Charter

A test charter provides focus and direction for an exploratory session without restricting the tester's creativity. It defines the target, the tools, and what to look for.

### Example Charter Template
* **Mission:** Explore the checkout flow for usability, validation errors, unclear messages, and unexpected user behavior.
* **Focus Areas:**
    - Invalid payment data
    - Empty mandatory fields
    - Navigation backwards and forwards
    - Session timeout
    - Error recovery

## 5. Notes and Evidence

## 6. Example Exploratory Session

**Session Date:** June 14, 2026 | **Duration:** 45 Minutes | **Tester:** Lucinda

### Real-Time Session Log (Based on Section 4 Charter)
* **[00:05] Focus - Empty mandatory fields:** Attempted to bypass the shipping form by clicking "Next" with empty fields. Inline validation triggered successfully, but field borders did not turn red (minor usability issue).
* **[00:18] Focus - Navigation backwards and forwards:** Filled out payment details, clicked "Review Order", then used the browser's back button. *Bug found:* The credit card field was completely cleared, forcing the user to re-type the 16-digit number.
* **[00:32] Focus - Error recovery:** Turned off network connection mid-transaction to test error recovery. The UI spinner spun indefinitely instead of timing out or showing a "Network lost, please retry" message.

## 7. Findings Template