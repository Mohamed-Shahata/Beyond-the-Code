# 06: Solution

This is a model solution, not the only correct answer. If you found a point that is not listed here, that is a good sign.

## 1) The Six Questions

| Question | Answer |
|---|---|
| Customer and User | The customer orders and pays. Users: the customer, the courier, laundry staff, the admin |
| Problem solved | The customer saves time: no trip to the laundry and no waiting |
| Money | The customer pays by weight and wash type, cash to the courier or online. Monthly subscriptions are steady income, and compensation is a cost |
| Core operations | Request a pickup, pick up and weigh, wash, deliver, pay |
| Rules | Pricing by weight and type, subscription discount, compensation for damage |
| Other parties | Payment Gateway, a notification service (SMS or similar) |

## 2) Order Statuses

```mermaid
stateDiagram-v2
    [*] --> Requested
    Requested --> PickupScheduled
    PickupScheduled --> PickedUp
    PickedUp --> InLaundry
    InLaundry --> Ready
    Ready --> OutForDelivery
    OutForDelivery --> Delivered
    Requested --> Cancelled
    PickupScheduled --> Cancelled
```

Note: the payment state (Paid or Unpaid) can be kept separate from the order status, because cash is collected at a different point depending on the customer's choice.

## 3) Questions for the Business

| ID | Question | Why do we need to know? |
|---|---|---|
| Q-01 | The price is set after weighing. If the customer rejects the price, is the order cancelled or does it continue? | Affects order statuses and cancellation |
| Q-02 | Up to which status is cancellation allowed? | Statuses and refunds |
| Q-03 | How is compensation calculated, and who approves it? | A financial Business Rule that needs permissions |
| Q-04 | Does the monthly subscription have a weight cap? What happens if the customer goes over it or doesn't use it all? | Defines discount calculation and rollover |
| Q-05 | When does the courier hand the collected cash to the laundry? | Affects accounting and reporting |

## What You Took Away from This Part

- There are six fixed questions that unlock any Business.
- Order statuses are the easiest way to see all the operations in one diagram.
- Most of the ambiguity you find is a Business decision, and its place is the Question Log.

Next part: System Design.

---

Previous: [05](./05-exercise.md) | Home: [README](../README.md)
