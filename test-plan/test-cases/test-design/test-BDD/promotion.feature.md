# Module Summary: Promotion System
## Overview

The Promotion System module is responsible for applying discounts to users based on their active registration time.

This module ensures that eligible users receive the correct discount percentage during the checkout process, following predefined business rules.

# Feature: Promotion System

## Business Rule

**BR-01:** Users must receive discounts based on their active registration time:

* Less than 5 years → 10% discount
* Between 5 and 10 years → 20% discount
* More than 10 years → 50% discount

**BR-02:** The discount must be applied only to the next two products added to the cart during checkout.

---

# BDD-01

## Scenario: Apply 10 percent discount for users with less than 5 years

Given the user has 2 years of active registration
And the user has added 2 products to the cart

When the user proceeds to checkout

Then the system should apply a 10 percent discount to both products

---

# BDD-02

## Scenario: Apply 20 percent discount for users between 5 and 10 years

Given the user has 7 years of active registration
And the user has added 2 products to the cart

When the user proceeds to checkout

Then the system should apply a 20 percent discount to both products

---

# BDD-03

## Scenario: Apply 50 percent discount for users with more than 10 years

Given the user has 15 years of active registration
And the user has added 2 products to the cart

When the user proceeds to checkout

Then the system should apply a 50 percent discount to both products
