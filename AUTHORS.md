Authors ordered by first contribution.

SungMin Ha (ishtar aka iziz, zen.isis@gmail.com)
Hyuk Hur (hyukhur@gmail.com)

Cliff Rowley (cliffrowley@gmail.com)
  - Missing return value in formatInOriginalFormat:regionCallingFrom:error
  - Compatibility with iOS versions prior to 6.x

Aaron Wojnowski (aaronwojnowski@gmail.com)
  - Remove extra r from the countryCodeFromRegionCode method name.

stonyw
  - Handle char @ when normalize any strings, eg email

Yosi Taguri (http://ahhhpah.com)
  - Failed tests are down to 18 for [ AsYouTypeFormatter ]

Nils Hayat (http://nilsou.com)
  - Help to update cocoapods
  - Added -[NBPhoneNumberUtil parseWithPhoneCarrierRegion:error:] to parse a number using the phone's carrier country code

Frane Bandov frane (frane@offbyte.com, http://frane.offbyte.com)
  - Refactor to reduce memory consumption
  	(Export NSArray category into separate files,
  	Optimize constants,
  	Cache regex patterns to reduce memory and CPU consumption,
  	Make countyCodeByCarrier method publically available,
  	Add libPhoneNumber.{h,m} to podspec)

Cliff Ingham (inghamn@bloomington.in.gov, http://bloomington.in.gov/)
  - Added explicit type casts to avoid warnings when building for 64 bit iOS...

rhoiberg
  - Allow NBPhoneNumberUtil to be created using a specified bundle.

Google Inc.
  - Add some digits mapping.
  - Reduce Library Size by compiling data directly into binary instead of generating a class per region.
