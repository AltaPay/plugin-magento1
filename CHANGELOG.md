# Changelog
All notable changes to this project will be documented in this file.

## [3.1.7]
**Fixes**
- Fix: Order mismatch issue in case of PayPal orders.

## [3.1.6]
**Fixes**
- Fix orderline mismatch issue with capture payment.

## [3.1.5]
**Improvements**
- Added configuration to redirect to cart or on a separate fail page on error

## [3.1.4]
**Improvements**
- Support redirect with PayPal payment method

## [3.1.3]
**Fixes**
- Fix: Order grid showing wrong payment information

## [3.1.2]
**Fixes**
- Use `subscription` as auth type instead of `recurring`
- Fixed Internal Server Error from notification call
    
## [3.1.1]
**Improvements**
- Support for multi-site payment

## [3.1.0]
* Removed MOTO functionality due to Magento 1 EOL and PCI compliance

## [3.0.0]
**Improvements**
- Added plugin disclaimer
- Major refactoring for improving the source code quality
- Added cancel order functionality
- Refactored shipping tax percentage method, due to the deprecation for versions above 1.9.2
- Revamped the quote conversion to order logic
- Added support for Downloadable products with customs prices
- Added support for Klarna Payments (Klarna reintegration)
- Tracking info sent at capture call, if available
- Improved functionality for credit card token usage

**Fixes**
- Empty payment method tile shown in the checkout if the title is not configured
- Order not canceled if the payment is released by the payment gateway
- Zero amount items not sent as orderlines
- Bundle products with fixed price not included in the orderlines
- Order not saved and exception is thrown if quote is not converted into order

## [2.11.1]
**Fixes**
- Broken credit card token functionality
- MobilePay orders created under certain situations cannot be captured from the admin panel

## [2.11.0]
**Improvements**
- Added support for discounts when coupon with fixed amount

**Fixes**
- Capture failing on certain orders created with MobilePay
- Partial captures failing when compensation amount involved
- Email with successful order not sent when only notification callback is triggered
- Order status not changing from Canceled to Processing if successful payment
- Original price shown in the order details

## [2.10.0]
**Improvements**
- Added full support for multiple tax rates
- Various improvements in order to support a certain gift card plugin

**Fixes**
- Discounts and tax amounts with more than two digits

## [2.9.1]
**Fixes**
- Potential quote duplicates at order creation
- Performance fix at load order and redirect to success page

## [2.9.0]
**Improvements**
- Orders created before payment page to avoid missing orders
- Full support for configurable products
- Revamp orderlines for capture and refund calls
- Final updates related to the branding changes

**Fixes**
- Correctly handling of the open notification callback

## [2.8.0]
**Improvements**
- Additional improvements for bundle products
- Added support for:
    - configurable products with fixed price
    - customer tax after discount configuration
    - multiple catalog discounts
    - amounts with more than two digits (payment gateway limitation)

**Fixes**
- Missing shipping details or phone number, when 3rd party plugins used, at order creation
- Hijacked sessions issue

## [2.7.0]
**Improvements**
- Added support for bundle products
- Multiple enhancements related to various types of discounts
- Added support for shipping discounts
- Shipping can be refunded as a regular order line
- Added a list of limitations(subject to changes)

**Fixes**
- Failed partial captures and refunds when Klarna used
   
## [2.6.1]
**Fixes**
- Shipping details not correctly read from the payment gateway payload

## [2.6.0]
**Improvements**
- Parse the shipping details, from the payment gateway, at order creation when shipping modules are used

## [2.5.0]
**Improvements**
-  Added logs in key places

**Fixes**
- Payment information not shown in the order view
- Missing or duplicated orders due to various reasons

## [2.4.1]
**Fixes**
- Error page shown on successful MobilePay payment

## [2.4.0]
**Improvements**
- Major refactoring in the notificationAction flow
	- no redirected to successAction is being made, the order is created separately
- Handling discounts, particularly on price including tax
- Updates in terms of logging, for a better overview when something fails

**Fixes**
- Unit price not fetched correctly on price including taxes

    **Note:**
    - The discounts cannot be properly fetched when following scenarios: Catalog prices: excluding tax, Apply customer tax: after discount, apply discount on prices:
        - including tax
        - excluding tax

## [2.3.0]
**Improvements**
- Added support for Gift Cards
- Added support for price rule discount in combination with cart discount

**Fixes**
- Wrong total amount when comma is used as decimal on numbers over 3 digits
- Unit price including the tax amount in certain situations

## [2.2.0]
**Improvements**
- Added cart discount as a separate orderline, aligned with the payment gateway
- PHP SDK updates in order to perform captures on MOTO orders
- MOTO orders improvements:
    - capture is now possible
    - added more details (customer and transaction information) when order is created in the payment gateway

**Fixes**
- Plugin versioning correctly parsed across all calls to the payment gateway
- Success action: reserve ID matching with the one from the createPayment request
- Notification action

    **Note:** Only discounts in percentage, two digits, are supported for payments made with Klarna

## [2.1.0]
**Improvements**
- Stronger solution for handling thousand and decimal separators
- Payment method displayed properly, along with the currency under "Payment information" section

**Fixes**
- Capture online failing on orders created before rebranding changes update
- Create CreditMemo functionality broken

## [2.0.0]
**Improvements**
- Invoice automatically created when ePayment is used

**Fixes**
- Cart is not cleared after the order is created
- Missing orders when consumer logs into account during the checkout process

## [1.9.0]
**Improvements**
- Branding changes from Altapay to Valitor
- Platform and plugin versioning information sent to the payment gateway

**Fixes**
- Capture functionality failing due to wrong serialization

## [1.8.0]
**Improvements**
- Send tax information for the shipping items
- Update the PHP SDK

**Fixes**
- Terminal name shown correctly in the checkout page
- The payment fetched correctly in the success Action
- The order is created correctly

## [1.7.2]
- Platform improvements

## [1.7.1]
- Improvements related to serialization

## [1.7.0]
- Updates related to PHP SDK

## [1.6.0]
- Updates in PHP SDK in order to support "PaymentSource" Transaction child element in Payment Gateway requests/responses

## [1.5.0]
- Configured PHP SDK reference through composer

## [1.4.0]
- Logging functionality updates

## [1.3.1]
- Implemented async http calls feature
- Changed release and refund methods to use async http calls when handling transaction rejection

## [1.3.0]
- Implemented Address Verification (AVS) Check function for orders

## [1.2.1]
- Correction of a bug in the order lines

## [1.2.0]
- Merging of two modules: Altapay_Payment_v1.1.3 and Altapay_PaymentExtraGateways_v1.0.1.
    - Both modules were implemented by Tric Solutions.

## [1.1.3]
- Bug fix regarding the selection of payment action

## [1.1.2]
- Implementation of customer choice to save credit card token in payment window

## [1.1.1]
- Conflict handling with Pensio Module
- Correct terminal choice when using StoreCreditcard / recurring

## [1.1.0]
- Handling of customer creation on order create.

## [1.0.2]
- Minor bug fixes

## [1.0.1]
- Implementation of Tokenization

## [1.0.0]
- Fork of Pensio_Payment 1.3.0