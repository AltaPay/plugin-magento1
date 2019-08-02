# ValitorOmni for Magento plugin

Integrating with Valitor could not be easier. Choose between Hosted, HTTP POST or XML integration options, or
alternatively browse our selection of client libraries and e-commerce platform modules. Imagine having full
creative control over payment flow, checkout design, and A/B testing without any card data risk.

## Supported functionalities
![skaermbillede 2016-03-02 kl 15 24 29](https://cloud.githubusercontent.com/assets/17084032/13463104/fbd50f90-e08a-11e5-90c1-60d1ace4216a.png)

## Supported versions
Magento 1.X

## Contact
Feel free to contact our partnership team (partnerships@valitor.com) if you need any assistance.

## Change log

!!! Important note related to the branding changes: please uninstall the Altapay plugin before installing the newer version (greater than 1.8.0)!

2.4.1
* Bug fixture
    - Error page shown on successful MobilePay payment

2.4.0
* Improvements
	- Major refactoring in the notificationAction flow
		- no redirected to successAction is being made, the order is created separately
	- Handling discounts, particularly on price including tax
	- Updates in terms of logging, for a better overview when something fails
* Bug fixtures
	- Unit price not fetched correctly on price including taxes
* Note
	- The discounts cannot be properly fetched when following scenarios: Catalog prices: excluding tax, Apply customer tax: after discount, apply discount on prices:
		- including tax
		- excluding tax

2.3.0
* Improvements
    - Added support for Gift Cards
    - Added support for price rule discount in combination with cart discount
* Bug fixtures
    - Wrong total amount when comma is used as decimal on numbers over 3 digits
    - Unit price including the tax amount in certain situations

2.2.0
* Improvements
    - Added cart discount as a separate orderline, aligned with the payment gateway
    - PHP SDK updates in order to perform captures on MOTO orders
    - MOTO orders improvements:
    	- capture is now possible
    	- added more details (customer and transaction information) when order is created in the payment gateway
* Bug Fixtures:
	- plugin versioning correctly parsed across all calls to the payment gateway
	- success action: reserve ID matching with the one from the createPayment request
	- notification action
* Note:
	- Only discounts in percentage, two digits, are supported for payments made with Klarna

2.1.0
* Improvements
    - Stronger solution for handling thousand and decimal separators
    - Payment method displayed properly, along with the currency under "Payment information" section
* Bug fixtures
    - Capture online failing on orders created before rebranding changes update
    - Create CreditMemo functionality broken

2.0.0
* Improvements
    - Invoice automatically created when ePayment is used
* Bug fixtures
    - Cart is not cleared after the order is created
    - Missing orders when consumer logs into account during the checkout process

1.9.0
* Improvements
    - Branding changes from Altapay to Valitor
    - Platform and plugin versioning information sent to the payment gateway
* Bug fixtures
    - Capture functionality failing due to wrong serialization

1.8.0
* Improvements
    - Send tax information for the shipping items
    - Update the PHP SDK
* Bug fixtures
    - Terminal name shown correctly in the checkout page
    - The payment fetched correctly in the success Action
    - The order is created correctly

1.7.2
* Platform improvements

1.7.1
* Improvements related to serialization

1.7.0
* Updates related to PHP SDK

1.6.0
* Updates in PHP SDK in order to support "PaymentSource" Transaction child element in Payment Gateway requests/responses

1.5.0
* Configured PHP SDK reference through composer

1.4.0
* Logging functionality updates

1.3.1
* Implemented async http calls feature
* Changed release and refund methods to use async http calls when handling transaction rejection

1.3.0
* Implemented Address Verification (AVS) Check function for orders

1.2.1
* Correction of a bug in the order lines

1.2.0
* Merging of two modules: Altapay_Payment_v1.1.3 and Altapay_PaymentExtraGateways_v1.0.1.
    - Both modules were implemented by Tric Solutions.

1.1.3
* Bug fix regarding the selection of payment action

1.1.2
* Implementation of customer choice to save credit card token in payment window

1.1.1
* Conflict handling with Pensio Module
* Correct terminal choice when using StoreCreditcard / recurring

1.1.0
* Handling of customer creation on order create.

1.0.2
* Minor bug fixes

1.0.1
* Implementation of Tokenization

1.0.0
* Fork of Pensio_Payment 1.3.0