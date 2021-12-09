# objc-libphonenumber-spm

A fork of [iziz/libPhoneNumber-iOS](https://github.com/iziz/libPhoneNumber-iOS) updated to work flawlessly as the Swift Package library. Includes PhoneNumberUtil, ShortNumberUtil, AsYouTypeFormatter, but does not include a Geocoder. The package is not extensively tested yet, and test targets are not ported from original repo.

Whenever needed, pass the metadataHelper explicitly during initialization, otherwise the instance won't initialize propoerly.

```swift
final class PhoneUtils {

  private let phoneUtil: NBPhoneNumberUtil
  private let asYouType: NBAsYouTypeFormatter
  private let shortNumberUtil: NBShortNumberUtil
  
  init() {
    let metadataHelper = NBMetadataHelper()!
    let shortNumberMetaDataHelper = NBShortNumberMetadataHelper()
    let phoneUtil = NBPhoneNumberUtil(metadataHelper: metadataHelper)!
    
    self.phoneUtil = phoneUtil
    self.asYouType = .init(regionCode: Locale.current.regionCode)
    self.shortNumberUtil = .init(metadataHelper: shortNumberMetaDataHelper, phoneNumberUtil: phoneUtil)
    }
    
    // wrap the methods you need for your usecases
    //
    //
}
```
