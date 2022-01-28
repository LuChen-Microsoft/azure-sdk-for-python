# Release History

## 1.0.0b1 (Unreleased)

This version and all future versions will require Python 3.6+. Python 2.7 is no longer supported.

### Features Added

- This package follows from the azure-schemaregistry-avroserializer.
- APIs have been updated to allow for encoding directly to and decoding from message type objects, where the data value is the Avro encoded payload.
- The schema ID and format indicator are no longer prepended to the payload. Instead, the content type of the message will hold this information.

### Breaking Changes

### Bugs Fixed

### Other Changes

- This beta release will be backward compatible for decoding data that was encoded with the AvroSerializer.
- The `encode` and `decode` methods on `AvroEncoder` support the following message models:
  - `azure.eventhub.EventData` in `azure-eventhub==5.9.0b1`