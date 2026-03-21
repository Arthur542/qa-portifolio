# Test Design – Evidence Summary

This module contains evidence of test design techniques applied to validate system behavior through structured approaches.

The following techniques were used:

## Boundary Value Analysis (BVA)

Focuses on testing input limits where defects are more likely to occur.
Evidence demonstrates how the system behaves at minimum and maximum boundaries, including both valid and invalid scenarios.

## Equivalence Partitioning (EP)

Focuses on dividing input data into valid and invalid groups.
Evidence demonstrates how the system handles representative inputs from each partition.

---

The evidence presented includes selected scenarios that best represent each technique, ensuring clarity without redundancy.

These tests were designed to validate input fields such as username and password, covering both valid and invalid conditions.

---

# Test Design – Boundary Value Analysis (BVA)

This section presents test scenarios based on Boundary Value Analysis, focusing on validating the limits of the username field.

## Rule

* Username must contain between **6 and 30 characters**

---

## Selected Evidence Scenarios

To demonstrate the application of BVA, key boundary scenarios were selected, including invalid and valid edge cases.

---

### Scenario: Username with 5 characters (Minimum - 1)

Validates behavior when the input is below the minimum allowed length.

Expected Behavior:
The system should reject the input and display a validation message.

Evidence:

![BVA Invalid Minimum](../images/minimum-username-1.png)

---

### Scenario: Username with 6 characters (Minimum)

Validates the lowest valid boundary value.

Expected Behavior:
The system should accept the input.

Evidence:

![BVA Valid Minimum](../images/minimum-username.png)

---

### Scenario: Username with 30 characters (Maximum)

Validates the highest valid boundary value.

Expected Behavior:
The system should accept the input.

Evidence:

![BVA Valid Maximum](../images/maximum-username.png)

---

These scenarios highlight how the system behaves at critical boundary limits, where defects are more likely to occur.

# Test Design – Equivalence Partitioning

This section presents test scenarios based on Equivalence Partitioning, focusing on validating the password field.

## Rule

* Password must contain at least **8 characters**
* System should accept valid inputs within acceptable limits

---

## Partitions Identified

* Valid Inputs: Passwords with sufficient length (e.g., 50 characters)
* Invalid Inputs: Passwords below minimum length

---

## Selected Evidence Scenarios

To demonstrate the application of Equivalence Partitioning, representative scenarios from each partition were selected.

---

### Scenario: Password with less than 8 characters

Validates behavior when the input does not meet the minimum requirement.

Expected Behavior:
The system should reject the input and display a validation message.

Evidence:

![EP Invalid Password](../images/ep-invalid-password.png)

---

### Scenario: Password with 50 characters

Validates a valid input within the acceptable range.

Expected Behavior:
The system should accept the input.

Evidence:

![EP Valid Password](../images/ep-valid-password.png)

---

These scenarios demonstrate how the system handles different input groups, ensuring correct validation for both valid and invalid data.


