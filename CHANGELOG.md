## 1.2 (2024-09-13)
- This release adds the ability to cancel a transaction before payment is presented, as opposed to waiting for the reader to timeout. Simply call the new `cancelTransaction()` function after a transaction has begun but before the card is presented. If the reader is successully able to cancel the operation, the `charge()` function will throw a `CloverTransactionError` with a code of `.cancelled`. If a card has already been presented, the payment may be completed— at which time, you may reverse the payment as needed.
- Also includes miscellaneous bug fixes and improvements.

## 1.1.3 (2024-08-27)
- This release adds additional internal tools to assist Clover Developer Relations in debugging. No external or public changes.

## 1.1.2 (2024-07-11)
- This release fixes an issue where the `employeeId` associated with a payment might be invalid, resulting in rejected payments.

## 1.1.1 (2024-06-20)
- Improved the linking of some of our internal dependencies to address an App Store validation issue. No code, API, or functionality changes from 1.1.0.

## 1.0.3 (2024-06-18)
- Improved the linking of some of our internal dependencies to address an App Store validation issue. No code, API, or functionality changes from 1.0.2.

## 1.1.0 (2024-05-20)

- Added support for OAuth V2 Tokens (https://docs.clover.com/docs/oauth-intro)
- Added support for external OAuth flows (NoOAuth)
- Improved retries to inititial sequence of data fetches to improve startup reliability
- Added privacy manifest
- Other minor bug fixes

## 1.0.2 (2024-04-24)

- SDK can now be initialized and logged into using the simulator (payment and bluetooth operations are not possible on the simulator).
- Added support for new Clover staging environment.
- Fixed a crash that can occur during SDK initialization.
- Other minor bug fixes


## 1.0.1 (2024-02-05)

No code changes: updating the CHANGELOG and README links to point at the raw .md files on Github so that the Cocoapods metadata service correctly parses them.

## 1.0.0 (2024-02-02)

Initial non-beta, public release
