# User Story 001: [User Registration]

**ID:** US-002  
**Role:** Registered Customer

---

## Description

A brief summary of the user story:

> As a registered customer I want to login with my email and password So that I can access my account and place orders.

---

## Acceptance Criteria

Specific conditions that must be met for this user story to be considered complete:

- User enters valid email and password
- System authenticates credentials against database
- Session is created upon successful login (expires after 24 hours of inactivity)
- User is redirected to homepage or intended destination
- Failed login attempts are tracked (max 5 attempts before 15-minute lockout)
- User can choose "Remember Me" option (extends session to 30 days)

---

## Flowchart

High-level visual representation of the process:

<div align=center>

![Flowchart](./flowchart.png)

 </div>

## Sequence Diagram

Illustrates the step-by-step interaction between actors and the system:

<div align=center>

![Sequence Diagram](./sequence-diagram.png)

 </div>

## Pseudocode

```text
function string authenticateCustomer(custCredentials){
    Customer customer = findCustomer(custCredentials); // DB call

    if customer is null // means not found (invalid email or password)
        Throw new Error("Invalid Email or Password");

    if customer choosed Remember Me option
        return session valid for 30 days

    return session valid for 24 hours;
}
```
