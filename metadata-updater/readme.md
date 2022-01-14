## Updating the metadata

This directory contains scrips from the original libphonenumber-objc repository that are needed to update the metadata and generate corresponding headers.

Below is short how-to manual that's useful for updating the metadata without relying on this package distribution. Please note: the procedures have not been properly tested and may not produce the valid outcome.


###  Run the metadataGenerator script from within the `metadata-updater` directory:

```
./metadataGenerator.swift
```

Upon completion, a `generatedJSON` folder will contain three metadata files, namely:

- PhoneNumberMetaData.json
- PhoneNumberMetaDataForTesting.json
- ShortNumberMetadata.json

Note that a Javascript exception maybe logged into console, which does not seem to impact the result.


### Run the GeneratePhoneNumberHeader script from within the generatedJSON folder:

```
cd generatedJSON
```
```
./GeneratePhoneNumberHeader.sh
```

Upon completion, a `NBGeneratedPhoneNumberMetaData.h` header file will be created.


### Manually update the data in corresponding metadata headers in libphonenumber directory:

The metadata headers are contained both in headers (Internal) and Sources directories so make sure to update the values accordingly.

The generated header contains values for testing (smaller in size), actual phone-number metadata, and short-number metadata. 

```NBGeneratedPhoneNumberMetaData``` header holds the phone-number metadata inside these variables:

```
kPhoneNumberMetaData
kPhoneNumberMetaDataCompressedLength
kPhoneNumberMetaDataExpandedLength
```

```NBGeneratedShortNumberMetadata``` header holds the short-number metadata inside these variables:

```
kShortNumberMetaData
kShortNumberMetaDataCompressedLength
kShortNumberMetaDataExpandedLength
```
