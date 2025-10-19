# Boundary Test Data for Habi Heritage System

## Overview
This document contains boundary value test cases for the Habi Heritage web platform. Boundary testing verifies that the system correctly handles edge cases at the limits of acceptable input ranges.

## 1. Authentication Module

### Password Length Boundaries
- **Minimum Password Length (8 characters):** Password: "Pass123!" - Should accept
- **Maximum Password Length (128 characters):** Password: 128-character string - Should accept

### Email Format Boundaries
- **Minimum Email Length:** "a@b.c" - Should accept
- **Maximum Email Length:** 254-character email - Should accept

## 2. Product Catalog Module

### Price Boundaries
- **Minimum Price (0.01):** ₱0.01 - Should accept
- **Maximum Price (999999.99):** ₱999999.99 - Should accept

### Name Length Boundaries
- **Minimum Name Length (1 character):** "A" - Should accept
- **Maximum Name Length (255 characters):** 255-character string - Should accept

### Description Length Boundaries
- **Minimum Description Length (0 characters):** Empty - Should accept
- **Maximum Description Length (1000 characters):** 1000-character string - Should accept

## 3. Checkout Module

### Quantity Boundaries
- **Minimum Quantity (1):** 1 item - Should accept
- **Maximum Quantity (99):** 99 items - Should accept

### Total Amount Boundaries
- **Minimum Total (0.01):** ₱0.01 - Should accept
- **Maximum Total (999999.99):** ₱999999.99 - Should accept

### Customer Name Length Boundaries
- **Minimum Name Length (1 character):** "A" - Should accept
- **Maximum Name Length (255 characters):** 255-character string - Should accept

### Address Length Boundaries
- **Minimum Address Length (10 characters):** "123 Street" - Should accept
- **Maximum Address Length (500 characters):** 500-character string - Should accept

## 4. Donations Module

### Amount Boundaries
- **Minimum Donation (1.00):** ₱1.00 - Should accept
- **Maximum Donation (999999.99):** ₱999999.99 - Should accept

### Donor Name Length Boundaries
- **Minimum Name Length (0 characters):** Anonymous - Should accept
- **Maximum Name Length (255 characters):** 255-character string - Should accept

### Message Length Boundaries
- **Minimum Message Length (0 characters):** Empty - Should accept
- **Maximum Message Length (1000 characters):** 1000-character string - Should accept

## 5. Fundraising Module

### Goal Amount Boundaries
- **Minimum Goal (100.00):** ₱100.00 - Should accept
- **Maximum Goal (9999999.99):** ₱9999999.99 - Should accept

### Current Amount Boundaries
- **Minimum Current (0.00):** ₱0.00 - Should accept
- **Maximum Current (9999999.99):** ₱9999999.99 - Should accept

### Campaign Title Length Boundaries
- **Minimum Title Length (1 character):** "A" - Should accept
- **Maximum Title Length (255 characters):** 255-character string - Should accept

### Description Length Boundaries
- **Minimum Description Length (10 characters):** "Short desc" - Should accept
- **Maximum Description Length (2000 characters):** 2000-character string - Should accept

## 6. Gallery Module

### Title Length Boundaries
- **Minimum Title Length (1 character):** "A" - Should accept
- **Maximum Title Length (255 characters):** 255-character string - Should accept

### Description Length Boundaries
- **Minimum Description Length (0 characters):** Empty - Should accept
- **Maximum Description Length (1000 characters):** 1000-character string - Should accept

### Image File Size Boundaries
- **Minimum Size (1 KB):** 1KB image - Should accept
- **Maximum Size (5 MB):** 5MB image - Should accept

## 7. Storytelling Module

### Title Length Boundaries
- **Minimum Title Length (1 character):** "A" - Should accept
- **Maximum Title Length (255 characters):** 255-character string - Should accept

### Content Length Boundaries
- **Minimum Content Length (10 characters):** "Short story" - Should accept
- **Maximum Content Length (50000 characters):** 50000-character string - Should accept

### Author Name Length Boundaries
- **Minimum Author Length (1 character):** "A" - Should accept
- **Maximum Author Length (255 characters):** 255-character string - Should accept

### Link URL Length Boundaries
- **Minimum URL Length (10 characters):** "http://a.b" - Should accept
- **Maximum URL Length (2000 characters):** 2000-character URL - Should accept

### Video URL Length Boundaries
- **Minimum Video URL Length (10 characters):** "http://a.b" - Should accept
- **Maximum Video URL Length (2000 characters):** 2000-character URL - Should accept

## 8. Short Films Module

### Title Length Boundaries
- **Minimum Title Length (1 character):** "A" - Should accept
- **Maximum Title Length (255 characters):** 255-character string - Should accept

### Description Length Boundaries
- **Minimum Description Length (10 characters):** "Short desc" - Should accept
- **Maximum Description Length (1000 characters):** 1000-character string - Should accept

### Video File Size Boundaries
- **Minimum Size (1 MB):** 1MB video - Should accept
- **Maximum Size (100 MB):** 100MB video - Should accept

## 9. Home Content Module

### Title Length Boundaries
- **Minimum Title Length (1 character):** "A" - Should accept
- **Maximum Title Length (255 characters):** 255-character string - Should accept

### Content Length Boundaries
- **Minimum Content Length (10 characters):** "Short text" - Should accept
- **Maximum Content Length (5000 characters):** 5000-character string - Should accept

## 10. Database and API Boundaries

### String Field Lengths (General)
- **VARCHAR(255) fields:** 255 characters - Should accept
- **TEXT fields:** 65535 characters - Should accept
- **LONGTEXT fields:** 4294967295 characters - Should accept

### Numeric Field Boundaries
- **TINYINT:** 0-255
- **SMALLINT:** -32768 to 32767
- **INT:** -2147483648 to 2147483647
- **BIGINT:** -9223372036854775808 to 9223372036854775807
- **DECIMAL(10,2):** -99999999.99 to 99999999.99

### Date/Time Boundaries
- **DATE:** '1000-01-01' to '9999-12-31'
- **DATETIME:** '1000-01-01 00:00:00' to '9999-12-31 23:59:59'

### File Upload Boundaries
- **Image files:** 1KB to 5MB
- **Video files:** 1MB to 100MB
- **Document files:** 1KB to 10MB

## 11. Performance Boundaries

### Concurrent Users
- **Minimum Load (1 user):** Single user operations - Should handle
- **Maximum Load (100 concurrent users):** 100 simultaneous users - Should handle

### Response Time Boundaries
- **Minimum Acceptable (0.1s):** < 0.1 seconds for simple operations
- **Maximum Acceptable (2.5s):** < 2.5 seconds for complex operations

### Database Query Boundaries
- **Result Set Size:** 1 to 10000 records per query
- **Query Execution Time:** < 1 second for SELECT, < 5 seconds for complex operations

## 12. Security Boundaries

### Input Validation Boundaries
- **SQL Injection Prevention:** All inputs sanitized
- **XSS Prevention:** HTML entities escaped
- **CSRF Protection:** Tokens validated

### Session Boundaries
- **Session Timeout:** 15 minutes to 24 hours
- **Maximum Concurrent Sessions:** 5 per user

### Rate Limiting Boundaries
- **API Calls per Minute:** 60 requests per user
- **Login Attempts:** 5 attempts per 15 minutes

These boundary values ensure the system handles edge cases properly and maintains data integrity across all modules.