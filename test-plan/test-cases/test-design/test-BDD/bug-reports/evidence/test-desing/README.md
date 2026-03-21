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

