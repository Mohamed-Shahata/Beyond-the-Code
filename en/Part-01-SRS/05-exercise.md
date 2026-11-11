# 05: Exercise: A Small SRS for QuickCart

Estimated time: 15 minutes

The SRS below has deliberate gaps and conflicts. Read it using the same steps as [file 03](./03-how-to-read-srs.md) and answer the questions. Try not to open the solution until you finish, because the value of the exercise is finding the problems yourself.

---

## QuickCart: SRS v0.1

**Purpose:** An online (Web) store where customers buy products.

**Scope:** Browsing products, Cart, orders, payment. A mobile app is not part of this release.

**Users:** Customer, Admin.

**Integration:** A Payment Gateway for online payments.

| ID | Functional Requirements |
|---|---|
| FR-01 | A customer can register with an email and password. |
| FR-02 | An admin can add and edit products. |
| FR-03 | A visitor can add products to the cart without an account. |
| FR-04 | A registered customer can create an Order from the cart. |
| FR-05 | A customer can cancel an order before it is delivered. |
| FR-06 | An order cannot be cancelled after payment is confirmed. |
| FR-07 | A customer can pay online or by Cash on Delivery (COD). |

| ID | Non-Functional Requirements |
|---|---|
| NFR-01 | The system must be fast. |

---

## Questions

1. Summarize the project in 3 lines.
2. Who are the Actors? One of them is missing from the Users list.
3. What is wrong with NFR-01? Rewrite it. (The number is an example; the Business must confirm it.)
4. There are at least 3 conflicts or gaps. Find them.
5. Write a Question Log with 5 questions for the Business, and explain why each one matters.

---

Previous: [04](./04-cheat-sheet.md) | Next: [06: Solution](./06-solution.md)
