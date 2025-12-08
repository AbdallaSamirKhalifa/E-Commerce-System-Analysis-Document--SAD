# User Story 001: User Registration

**ID:** US-001  
**Role:** New Visitor

---

## Description

A brief summary of the user story:

> As a new visitor I want to create an account with email and password So that I can make purchases and track my orders.

---

## Acceptance Criteria

Specific conditions that must be met for this user story to be considered complete:

- User provides first name, last name, email, and password
- Email must be unique in the system
- Password must be at least 8 characters with 1 uppercase, 1 lowercase, 1 number
- System validates email format
- User receives confirmation email upon successful registration
- System Display a success message

---

## Flowchart

### High-level visual representation of the process:

<div align=center>

![Flowchart](./flowchart.png)

</div>

## Sequence Diagram

### Illustrates the step-by-step interaction between actors and the system:

<div align=center>

![Sequence Diagram](./sequence-diagram.png)

</div>

## Pseudocode

```text
function  manageUserRegistration(userInfo){
    if(!isValidInputs(userInfo))
        return "Invalid data!";

    saveToDatabase(userInfo);
    @async mailUser(userInfo.email);
}
function isValidInputs(userInfo){
    if(userInof.firstName.isEmpty())
        return false;

    if(userInof.lastName.isEmpty())
        return false;

    if(!isValidEmailFormat(userInof.email))
        return false;

    if(!isValidPassword(userInfo.password))
        return falsel;

    return true;


}

```
