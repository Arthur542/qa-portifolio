# Input Validation Test Cases

This document contains manual test cases designed to validate the system's input validation behavior.

## Business Rules

BR-VAL-01: The system must prevent login when an invalid password is provided.

BR-VAL-02: The system must prevent login when an invalid username is provided.

BR-VAL-03: The system must prevent form submission when required fields are empty.

## VAL-01 – Login with invalid password

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
User must be previously registered in the system.

**Test Steps:**

1. Access the website: https://the-internet.herokuapp.com/login
2. Access the login page  
3. Enter a valid username  
4. Enter an invalid password  
5. Click the "Login" button  

**Test Data:**

Username: tomsmith  
Password: SuperSecretPassword123  

**Expected Result:**  
The system should prevent access to the secure page and display an "Invalid credentials" message.

**Actual Result:**  
The system prevented access to the secure page and displayed the message correctly.

**Status:** Passed

---

## VAL-02 – Login with invalid username

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
The system must be accessible.

**Test Steps:**

1. Access the website: https://the-internet.herokuapp.com/login
2. Access the login page  
3. Enter an invalid username  
4. Enter a valid password  
5. Click the "Login" button  

**Test Data:**

Username: tomsmith123  
Password: SuperSecretPassword!  

**Expected Result:**  
The system should prevent access to the secure page and display an "Invalid credentials" message.

**Actual Result:**  
The system prevented access to the secure page and displayed the message correctly.

**Status:** Passed

---

## VAL-03 – Submit form with empty username field

**Type:** Negative  
**Priority:** High  
**Module:** Input Validation  
**Precondition:**  
User must be on the registration page with all other fields filled correctly.

**Test Steps:**

1. Access the website: https://accounts.google.com/lifecycle/steps/signup/name?continue=https://myaccount.google.com?utm_source%3Daccount-marketing-page%26utm_medium%3Dcreate-account-button&dsh=S1275079143:1774029772256352&flowEntry=SignUp&flowName=GlifWebSignIn&TL=AHU8sQsvP3J5xkWIYArXuQNXyiodDh_kIXZ9-LHDw2SOoyPblilGhuK5eV1-kwbA
2. Access the register page  
3. Fill all required fields correctly  
4. Leave the "Name" field empty  
5. Click the "Next" button  

**Test Data:**

Minimum characters allowed: 6  
Maximum characters allowed: 30  

**Expected Result:**  
The system should prevent progress and display an error message.

**Actual Result:**  
The system prevented the advance and displayed the error message correctly.

**Status:** Passed

---
