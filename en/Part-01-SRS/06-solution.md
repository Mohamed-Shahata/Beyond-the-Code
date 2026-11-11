# 06: Solution

This is a model solution, not the only correct answer. If you found a point that is not listed here, that is a good sign.

## 1) Project Summary

QuickCart is a Web store that lets a customer register, add products to a cart, create an order, and pay online or on delivery. The admin manages products. The system integrates with an external Payment Gateway, and the mobile app is outside the current release.

## 2) The Actors

- Customer
- Admin
- Payment Gateway: an external Actor, missing from the Users list.
- Visitor: appears in FR-03 but is not defined in the users list.

## 3) The Problem with NFR-01

"Fast" cannot be measured or tested. A better version:

> 95% of product listing requests respond in under X ms under a load of Y concurrent users.

X and Y are the Business's decision.

## 4) Conflicts and Gaps

| # | Problem | Explanation |
|---|---|---|
| 1 | FR-03 vs. FR-04 | A visitor can add to the cart without an account, but only registered customers can order. What happens when the visitor clicks Place Order? |
| 2 | FR-05 vs. FR-06 | Cancellation is allowed before delivery but forbidden after payment is confirmed. Online payment is confirmed before delivery, so which rule wins? And what about COD? |
| 3 | Inventory is missing | There is no requirement about stock, even though creating an order depends on it. |
| 4 | Payment failure | It is not stated what happens to the order if payment fails. |
| 5 | Order Statuses | There are no order statuses, so "before delivery" is unclear. |

## 5) Question Log

| ID | Question | Why do we need to know? |
|---|---|---|
| Q-01 | Can a visitor check out as a guest, or is an account required? | Resolves the conflict between FR-03 and FR-04 |
| Q-02 | Up to which exact status is cancellation allowed? | FR-05 and FR-06 conflict |
| Q-03 | Is stock reserved at order time or after payment? | Affects Inventory and Orders |
| Q-04 | If payment fails, how long does the order stay Pending? | Defines the order statuses |
| Q-05 | What is the required system speed? | Without a number, there is nothing to test |

## Is the SRS Ready for Implementation?

No. You can start on Authentication and Products because they are clear. But for Cart, Orders, and Payments, we first have to resolve the conflicts and answer the questions above, otherwise we build on assumptions that may change.

## What You Took Away from This Part

- How to read an SRS in steps instead of getting lost.
- How to find conflicts before you write code.
- How to turn ambiguity into questions instead of assumptions.

Next part: Understanding the Business.

---

Previous: [05](./05-exercise.md) | Home: [README](../README.md)
