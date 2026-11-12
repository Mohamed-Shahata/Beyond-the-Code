# 01: Why Understand the Business Before the Code?

Reading time: 4 minutes

## The Problem

Take this hypothetical example: a developer receives a food delivery app project. They build Restaurants, Orders, and Drivers. The code works and is well organized. After delivery, the client asks: "Where is the restaurant commission? Where is the driver's pay per delivery?"

The developer's code wasn't wrong. The mistake was never finding these questions in the first place, because they never understood how money moves in this kind of business.

## The SRS Alone Is Not Enough

In Part 01 we learned to read an SRS and pull questions out of it. But an SRS is usually written assuming you already understand the domain. If you don't, you read every word and still miss what is absent, because you don't know it is absent.

The difference between a developer who implements what is written and one who finds the gaps is that the second one understands the Business.

## What Is a Business Domain?

The Business Domain is the field the project works in: e-commerce, clinics, delivery, education, banking. Every domain has its own language and rules. A word like Booking means something different in a hotel than in a clinic, and Order means something different in a restaurant than in a factory.

## Most of Your Questions Are Business Questions

Go back to the Question Log from Part 01:

- When is stock deducted?
- Up to which status is cancellation allowed?
- If payment fails, what do we do?

None of them is technical. They are all Business decisions, and the Database and the API are built on their answers.

## You Don't Have to Be a Domain Expert

What is expected of you is to understand any new Business in a short time, even if it is the first time you hear about its field. That is done with a fixed set of questions, which is the topic of the next file.

---

Home: [README](../README.md) | Next: [02: Six Questions](./02-six-questions.md)
