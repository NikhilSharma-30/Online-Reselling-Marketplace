# Online Re-Selling Site – Database Design and Functionality

An online re-selling site is a platform where users can sell and purchase used items. This requires a well-structured database to manage the information related to users, their ads, and orders.

## Requirement Analysis

### 1. Product Management

The first requirement is to store and manage product information. The `PRODUCT` table contains information about the product, such as the product ID, name, condition, image, category, price, and quantity. The table should be designed to handle multiple images for a single product, and the category should be normalized to a separate table to avoid data redundancy.

### 2. User Profile Management

The second requirement is to store and manage user profiles. The `USERS` table contains information about the user, such as the user ID, first name, last name, email, and phone number. The phone number should be stored as a string to allow for international numbers. The table should also include fields for billing and shipping addresses to simplify the checkout process.

### 3. Order Management

The third requirement is to manage orders. The `ORDERS` table contains information about the order, such as the order ID, product ID, buyer ID, amount, order date, and status ID. The table should be normalized to handle multiple products in a single order, and the status ID should be normalized to a separate table to allow for easy tracking of order status.

### 4. Delivery Details

The fourth requirement is to manage delivery details. The `DELIVERY_DETAILS` table contains information about the delivery, such as the order ID, address, and expected arrival date. The table should be linked to the `ORDERS` table to ensure that the delivery details are accurate and up-to-date.

### 5. Payment Information

The fifth requirement is to manage payment information. The `CARD_DETAILS` table contains information about the user's payment card, such as the card number and bank name. The table should be linked to the `USERS` table to ensure that the payment information is accurate and up-to-date.

---

## Summary

In summary, the database design for an online re-selling site should be able to store and manage product information, user profiles, orders, delivery details, and payment information. The tables should be designed to avoid data redundancy and ensure data accuracy and consistency. The design should also be scalable and flexible to accommodate future growth and changes in the business requirements.

---

## Functional Requirements

To implement the above schema for an online re-selling site, several functionalities are required. These functionalities include:

- Creating ads
- Deleting ads
- Placing orders
- Canceling orders
- Updating user profiles
- Displaying delivery status
- Displaying available categories

These functionalities require different SQL queries and triggers to be implemented.

A trigger can be implemented to increase the view count of an ad. Similarly, a trigger can be implemented to display the delivery status when it changes. The database must also ensure data integrity by implementing referential integrity constraints to ensure that no data is lost or corrupted.

---

## Usability and Security

To make the site user-friendly, the system should be easy to navigate, and search functionalities should be implemented to make it easier for users to find what they are looking for. Additionally, the system should implement secure and durable mechanisms. 

Thus, this site requires:

- Careful planning and designing of a well-structured database
- Implementation of various SQL queries and triggers
- Implementation of security measures to protect users' sensitive information

