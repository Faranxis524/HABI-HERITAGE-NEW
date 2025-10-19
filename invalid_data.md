Invalid Test Data for Habi Heritage System

Overview
This document contains invalid input data sets for negative testing of the Habi Heritage web platform. These test cases are designed to verify proper error handling and validation.

1. Authentication Module

 Invalid User Registration
- Invalid Email Format:
  - Name: francis
  - Email: invalid-email
  - Password: Password123!
  - (Check) I agree to the Terms & Conditions
  - Expected Error: Please include an '@' in the email address. 'invalid-email' is missing an'@'.

- Weak Password:
  - Name: francis
  - Email: francisgonzales@gmail.com
  - Password: 123
  - (Check) I agree to the Terms & Conditions
  - Expected Error: Password must be at least 8 characters

- Empty Required Fields:
  - Name: (empty)
  - Email: (empty)
  - Password: (empty)
  - (Check) I agree to the Terms & Conditions
  - Expected Error: Please fill out this field.

 Not Check I agree to the Terms & Conditions
- Invalid Email Format:
  - Name: francis
  - Email: francisgonzales@gmail.com
  - Password: Password123!
  - (not Check) I agree to the Terms & Conditions
  - Expected Error: You must accept the Terms & Conditions to proceed

-Duplicate Email:
  - Name: francis
  - Email: francisgonzales@gmail.com 
  - Password: Password123!
  - Expected Error: The email has already been taken.


Invalid User Login
- Wrong Password:
  - Email: francisgonzales@gmail.com 
  - Password: WrongPassword123!
  - Expected Error: The provided credentials are incorrect.

- Non-existent Email:
  - Email: nonexistent@example.com
  - Password: Password123!
  - Expected Error: The provided credentials are incorrect.

- Empty Login Fields:
  - Email: (empty)
  - Password: (empty)
  - Expected Error: Please fill out this field.


2. Admin Product Catalog Module

Invalid Product Creation
- Negative Price:
  - Name: Invalid Product
  - Description: Test product
  - Price: -100
  - File type: jpg
  - Expected Error: Error saving product.

- Empty Name:
  - Name: (empty)
  - Description: Test product
  - Price: 100.00
  - File type: jpg
  - Expected Error: Please fill out this field.

- Price Too High:
  - Name: Expensive Product
  - Description: Test product
  - Price: 1000000
  - File type: jpg
  - Expected Error: Error saving product.

- **Invalid Image Format:**
  - Name: Product with Invalid Image
  - Description: Test product
  - Price: 500
  - Category: Test
  - Image: invalid.exe
  - Expected Error: Error saving product.

3. User Checkout Module

Invalid Checkout Process
- Empty Customer Name:**
  - Customer Name: (empty)
  - Email: francisgonzales@gmail.com
  - Phone: +63 9911223569
  - Address 1: 123 Rizal Street, Manila, Philippines
  - Postal Code: 4025
  - Expected Error: Please fill out this field.

- **Invalid Email:**
  - Customer Name: francis
  - Email: invalid-email
  - Phone: +63 
  - Address 1: 123 Rizal Street, Manila, Philippines
  - Postal Code: 4025
  - Expected Error: Please include an '@' in the email address. 'invalid-email' is missing an'@'.


4. User Donations Module

Invalid Donation Submission
- Negative Amount:
  - Amount: -500
  - Category: Community Development
  - Expected Error: Please enter a valid amount.

- Zero Amount:
  - Amount: 0
  - Category: Community Development
  - Expected Error: Please enter a valid amount.

5. Admin Fundraising Module

- Empty Title:
  - Title: (empty)
  - Description: Test campaign
  - Expected Error: Please fill out this field.

6. Admin Gallery Module

  - File Type: .pdf
  - Expected Error: Error saving gallery item.

7. Admin Storytelling Module

 Title: Art and the Cordillera Weaving Tradition
 Content: Detailed story about the history and techniques of abaca weaving
  Image URl: https://cdn.shopify.com/s/files/1/0415/7737/files/shutterstock_1063712081_480x480.jpg?v=1636919490
 Video Link: https://barongwarehouse.ph/blogs/barong-bridges/textile-art-and-the-abra-weaving-tradition-christy-mabute
 Author: Christy Mabute

Invalid Story Content
- **Empty Title:**
  - Title: (empty)
  - Content: Detailed story about the history and techniques of abaca weaving
  - Image URl: https://cdn.shopify.com/s/files/1/0415/7737/files/shutterstock_1063712081_480x480.jpg?v=1636919490
  - Video Link: https://barongwarehouse.ph/blogs/barong-bridges/textile-art-and-the-abra-weaving-tradition-christy-mabute
  - Author: Christy Mabute
  - Expected Error: Please fill out this field.

- **Empty Content:**
- **Empty Title:**
  - Title: Textile Art and the Cordillera Weaving Tradition
  - Content: (empty)
  - Image URl: https://cdn.shopify.com/s/files/1/0415/7737/files/shutterstock_1063712081_480x480.jpg?v=1636919490
  - Video Link: https://barongwarehouse.ph/blogs/barong-bridges/textile-art-and-the-abra-weaving-tradition-christy-mabute
  - Author: Christy Mabute
  - Expected Error: Please fill out this field.

8. Admin Short Films Module

Invalid Short Film Content

- Empty Title:
  - Title: (empty)
  - Video: Vid1.mp4
  - Expected Error: Please fill out this field.

- Unsupported Video Format:
  - Title: Traditional Cordillera Textile Weaving
  - Video: .pdf
  - Expected Error: Error saving shortfilm.

