# Bug Report: Postal Code Validation Failure

## Module Summary

This module validates the **input fields during the checkout process**, ensuring that user-provided data meets the required validation rules before proceeding.

Special focus is given to mandatory fields such as **Postal Code**, which must follow defined input constraints to ensure data accuracy.

---

## Business Rule

* The **Postal Code field must be validated** before allowing the user to proceed
* The system must reject incomplete or invalid postal codes
* The field must require a **valid and complete numeric input**
* The system must display an error message when validation fails

---

## Bug Details

* **ID:** BUG-02
* **Title:** Postal Code field accepts invalid input (single digit)
* **Type:** Input Validation Error
* **Module:** Checkout
* **Priority:** High
* **Severity:** High
* **Status:** Open

---

## Environment

* **Browser:** Google Chrome
* **Operating System:** Windows 11
* **Environment:** Test

---

## Precondition

* User is authenticated
* At least one product is added to the cart

---

## Steps to Reproduce

1. Access the website: https://www.saucedemo.com
2. Log in with valid credentials
3. Navigate to the products page
4. Select one or more products
5. Add product(s) to the cart
6. Open the cart
7. Proceed to checkout
8. Navigate to **"Checkout: Your Information"** page
9. Fill in first name and last name with valid data
10. Enter only **1 digit** in the "Postal Code" field
11. Click on **"Continue"**

---

## Test Data

* **Username:** standard_user
* **Password:** secret_sauce
* **name and surname:** standard user
* **Postal Code:** "1"

---

## Expected Result

The system must prevent the user from proceeding and display an error message indicating that the postal code is invalid or incomplete.

---

## Actual Result

* Entered value: "1"
* The system allows the user to proceed to the **Checkout Overview** page without validation

---

## Impact

* Invalid user data is accepted
* Data integrity is compromised
* Potential issues in shipping and order processing
* Lack of proper input validation

---
