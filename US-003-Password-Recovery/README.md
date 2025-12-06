# User Story 003: Password Recovery

**ID:** US-003  
**Role:** Registered Customer

---

## Description

A brief summary of the user story:

> As a registered customer I want to reset my password if I forget It So that I can regain access to my account.

---

## Acceptance Criteria

Specific conditions that must be met for this user story to be considered complete:

- User requests password reset via email
- System sends reset link valid for 1 hour
- User creates new password meeting security requirements
- Old password is invalidated immediately
- User receives confirmation email
- System logs password change event

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
function getPasswordResetLink(userEmail){
    if(!userExists(userEmail))
        return "User not found";

    Token token=new Token();
    token.expirationDate(currentTime + 1);

    saveResetPasswordToken(token, email); // DB call
    @async sendResetPasswordLink(userEmail, token); // we should have a background worker to check if the email is sent successfully.

    return "Email sent please check your inbox";
}

function resetPassword(newPassword, userEmail, token){

    if (isTokenExpired(token))
        return "expired token";

    if(!isValidPasswordFormat(newPassword))
        return "Invalid password format";


    updatePassword(userEmail, newPassword); // DB call it also invalidates the old password / the password should be hashed using SHA256 algorithm.
    invalidateToken(token);

   logPasswordChangeEevent(userEmail);
   @async sendConfirmationMail(userEmail); // will be checked by the background worker.

    return "Password changed successfully";
}

```
