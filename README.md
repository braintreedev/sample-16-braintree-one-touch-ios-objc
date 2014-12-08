# Braintree One Touch on iOS (Objective C)

This is an example of One Touch in the Braintree V.zero Client SDK for processing both PayPal in iOS applications. It comes with a minimal backened example written in Node.js that shows how to generate client tokens and how to process the payment method nonce.

This code sample is based on [Commerce Factory Sample #14](https://github.com/commercefactory/014-braintree-payment-ios-objc).

## Technology

This demo uses

* Xcode 6.1+
* [AFNetworking](http://github.com/AFNetworking/AFNetworking)
* [Braintree Client SDK for iOS](http://github.com/braintree/braintree_ios)
* [Cocoapods](http://cocoapods.org/): the dependency manager for Objective-C projects.
* [The Braintree Fake iOS Wallet](https://github.com/braintree/fake-wallet-app-ios)

The sample backend is written in Node.js and uses:

* Node 0.10.26 or higher
* The [Express](http://expressjs.com/) web framework
* The [Braintree Node SDK](http://github.com/braintree/braintree_node)

## Running the server

* In the `server` folder
	* Run `npm install` to install all dependencies
	* Run `npm start` to start the Express app
	* 

## Installing the Fake iOS Wallet

To use One Touch we want to install a fake wallet on your emulator or actual device for testing purposes.

* In the `fake-wallet-app-ios` folder
	* Run `pod install` to install al dependencies.
	* Open the newly created file `fake-wallet.xcworkspace` in your Xcode
	* Build the app and run it in your emulator or on your device
	* Stop the process but don't quit the emulator (leave the wallet on the emulated or real device)

## Running the mobile app (Device / Emulator)

* In the `client` folder
	* Run `pod install` to install all dependencies.
	* Open the newly created file `vzero.xcworkspace` in your XCode. 
	* Build the app and run it in your emulator or on your device
		* *Once the app started it will try to get the client token from your backend. Ensure that your server is already running before you launch the mobile application.*
	* Click on `Start Payment`
	* Select `PayPal`
	* The app will hand off to the fake wallet
	* Click on `Succeed` to fake a successful payment
	* Click on `Pay` to finish the transaction
	* You will see a message that says __"Transaction ID: [transaction_id]"__

## Useful links

* [Full documentation for the Braintree Client SDK for iOS+Node](https://developers.braintreepayments.com/ios+node/start/overview) 
* [Guide on One Touch for iOS and Node](https://developers.braintreepayments.com/ios+node/sdk/client/setup#register-a-url-type)
