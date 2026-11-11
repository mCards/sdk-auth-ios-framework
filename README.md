# mCards Auth SDK for iOS

Customer distribution of **AuthSDK 1.1.19**, tested with **CoreSDK 1.4.8**.
The SDK supports Auth0 authentication, session/token refresh and cardholder profile flows.
Requires iOS 14 or later.

## Install with Swift Package Manager

1. Add `https://github.com/mCards/sdk-auth-ios-framework` at version **1.1.19** and
   select the `AuthSDK` product.
2. Add `https://github.com/mCards/sdk-cards-ios-framework` at version **1.1.19** and
   select its `CoreSDK` product for the shared models. If the app already uses that
   package's `CardsSDK` product, CoreSDK is already supplied.
3. Remove any separate older CoreSDK/model package reference to avoid duplicate modules.

No Wantsa repository access is required. Applications that do not use card features can
select just the `CoreSDK` product from the Cards package.

```swift
import AuthSDK
import CoreSDK
```

## Auth0 setup

Configure the client ID, domain and audience assigned to your program/environment.
In the app target's URL Types, use `auth0` as the identifier and
`$(PRODUCT_BUNDLE_IDENTIFIER)` as the URL scheme, and register the corresponding callback
with your Auth0 application. Do not reuse another program's sample credentials.

See the [customer Cards demo](https://github.com/mCards/sdk-cards-ios-demo) for the shared
Auth0 integration pattern and [SDK documentation](https://mcards.readme.io/docs/mcards-sdk-overview).

## Release provenance

The XCFramework is copied unchanged from the pinned reference release recorded in
`RELEASE.json`; `.source-revision` records its source commit. Only customer-facing packaging
and documentation are maintained here. After merging the update, tag the merge commit
`1.1.19` to make this version available through Swift Package Manager.
