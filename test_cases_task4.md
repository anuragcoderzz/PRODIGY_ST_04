# Test Cases for SauceDemo Checkout Process (Edge Cases)

## Overview
These test cases are created for the SauceDemo e-commerce website (https://www.saucedemo.com/) to verify the checkout process, focusing on edge cases such as missing form fields, invalid data, and session timeout scenarios.

## Test Case 1: Checkout with Missing First Name
- **Test Case ID**: TC_01  
- **Test Description**: Verify that the checkout process fails if the first name field is missing.  
- **Preconditions**: User is logged in, has added at least one product to the cart, and is on the checkout information page.  
- **Test Steps**:  
  1. Leave the first name field blank.  
  2. Enter last name as "Doe".  
  3. Enter postal code as "12345".  
  4. Click the "Continue" button.  
- **Expected Results**: Error message displayed: "Error: First Name is required".

## Test Case 2: Checkout with Missing Postal Code
- **Test Case ID**: TC_02  
- **Test Description**: Verify that the checkout process fails if the postal code field is missing.  
- **Preconditions**: User is logged in, has added at least one product to the cart, and is on the checkout information page.  
- **Test Steps**:  
  1. Enter first name as "John".  
  2. Enter last name as "Doe".  
  3. Leave the postal code field blank.  
  4. Click the "Continue" button.  
- **Expected Results**: Error message displayed: "Error: Postal Code is required".

## Test Case 3: Checkout with Invalid Postal Code (Letters)
- **Test Case ID**: TC_03  
- **Test Description**: Verify that the checkout process fails if the postal code contains invalid data (e.g., letters).  
- **Preconditions**: User is logged in, has added at least one product to the cart, and is on the checkout information page.  
- **Test Steps**:  
  1. Enter first name as "John".  
  2. Enter last name as "Doe".  
  3. Enter postal code as "abcde".  
  4. Click the "Continue" button.  
- **Expected Results**: Error message displayed: "Error: Postal Code must contain only numbers".

## Test Case 4: Checkout with All Fields Missing
- **Test Case ID**: TC_04  
- **Test Description**: Verify that the checkout process fails if all required fields are missing.  
- **Preconditions**: User is logged in, has added at least one product to the cart, and is on the checkout information page.  
- **Test Steps**:  
  1. Leave the first name field blank.  
  2. Leave the last name field blank.  
  3. Leave the postal code field blank.  
  4. Click the "Continue" button.  
- **Expected Results**: Error message displayed: "Error: First Name, Last Name, and Postal Code are required".

## Test Case 5: Session Timeout During Checkout
- **Test Case ID**: TC_05  
- **Test Description**: Verify that the checkout process fails if the session times out due to inactivity.  
- **Preconditions**: User is logged in, has added at least one product to the cart, and is on the checkout information page.  
- **Test Steps**:  
  1. Enter first name as "John".  
  2. Enter last name as "Doe".  
  3. Enter postal code as "12345".  
  4. Wait for 30 minutes without any activity (simulating session timeout).  
  5. Click the "Continue" button.  
- **Expected Results**: Error message displayed: "Session expired. Please log in again". User is redirected to the login page.