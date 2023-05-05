---
template: overrides/main.html
title: Orders
---

# Orders

An Order is a crucial Cellmobs entity that plays a central role in facilitating transactions and commerce across the platform. It serves as a key component that connects various elements of the commerce process, including Shopping Carts, [Subscription Plans](/app-console/manage-subscriptions), [payment transactions](#payment-transactions), and [payment processors](#payment-processors).

Orders are generated from Shopping Carts and Subscription Plans, representing the items or services that users wish to purchase. When an order is processed, it gets associated with one or more payment transactions (`PayTransaction`), which are then submitted to the payment processor linked to the Organization (`PaymentProcessor`). This ensures that the payment is securely handled and processed according to the platform's standards.

Cellmobs supports various payment processors, including Stripe, Authorize.net, FirstData, and PayPal. This allows organizations to choose their preferred payment processor and cater to the needs of their customers accordingly.

In addition to traditional payment methods, Cellmobs also supports virtual currencies, offering an alternative means of payment. Virtual currencies can be used as an abstraction for Fiat currencies, providing additional flexibility in payment options and catering to the growing demand for alternative payment methods.


## Viewing &amp; Managing Orders

## Shopping Carts

### Submitting Carts
 
### Editing Carts

## Subscription Plans

### Plan Product

### Subscriptions

## Payment Processors

### Payment Transactions

