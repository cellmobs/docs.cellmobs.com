---
template: overrides/main.html
title: Orders
---

# Orders

An Order is a crucial Cellmobs entity that plays a central role in facilitating transactions and commerce across the platform. It serves as a key component that connects various elements of the commerce process, including Shopping Carts, [Subscription Plans](/app-console/manage-subscriptions), [payment transactions](#payment-transactions), and [payment processors](#payment-processors).

Orders are generated from Shopping Carts and Subscription Plans, representing the items or services that users wish to purchase. When an order is processed, it gets associated with one or more payment transactions (`PayTransaction`), which are then submitted to the payment processor linked to the Organization (`PaymentProcessor`). This ensures that the payment is securely handled and processed according to the platform's standards.

Cellmobs supports various payment processors, including [Stripe](https://stripe.com/docs){:target=_blank}, [Authorize.net](https://www.authorize.net/){:target=_blank}, [FirstData](https://globalgatewaye4.firstdata.com/){:target=_blank}, and [PayPal](https://developer.paypal.com/home){:target=_blank}. This allows organizations to choose their preferred payment processor and cater to the needs of their customers accordingly.

In addition to traditional payment methods, Cellmobs also supports virtual currencies, offering an alternative means of payment. Virtual currencies can be used as an abstraction for Fiat currencies, providing additional flexibility in payment options and catering to the growing demand for alternative payment methods.


## Viewing &amp; Managing Orders

## Shopping Carts

### Submitting Carts
 
### Editing Carts

## Subscription Plans

### Plan Product

### Subscriptions

## Payment Processors

Cellmobs has built-in support for multiple payment processors (aka payment gateways), providing a flexible and versatile approach to handle transactions within your application. 

In a single-vendor application, you might configure a primary payment processor for your application and then add additional ones as backups. This is useful because it can provide a fallback option if there are issues with the primary processor, ensuring that your application can continue to accept payments without interruption.

<figure markdown>
![Payment Gateways](../assets/app-console/manage-processors.png){loading=lazy}
    <figcaption>Organization Payment Processors</figcaption>
</figure>

However, in a multi-vendor or marketplace environment, Cellmobs provides a different approach. In such a scenario, you can allow individual sellers or vendors (represented by Organizations within Cellmobs) to configure their own payment processors. This means each vendor in your marketplace can choose the payment processor that best suits their needs or preferences.

<figure markdown>
![Edit Payment Gateway](../assets/app-console/add-processors.png){loading=lazy}
    <figcaption>Edit Payment Processors Credentials</figcaption>
</figure>

In either case, the payment processor associated with the selling Organization is used when an order is being processed. This ensures that the money from the sale goes to the correct party.

By supporting multiple payment processors and allowing for flexible configuration, Cellmobs ensures that your application can effectively and efficiently handle transactions, providing a smooth and frictionless experience for both sellers and buyers.

### Payment Transactions

<br><br>