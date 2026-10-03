# VoiceConsent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**granted** | **boolean** | The speaker authorized creation and use of this voice. | [default to undefined]
**language** | **string** |  | [optional] [default to undefined]
**recording_uri** | **string** | Absolute media URI. Inline media uses a base64 data URI. | [optional] [default to undefined]

## Example

```typescript
import { VoiceConsent } from 'mm-gateway-ts';

const instance: VoiceConsent = {
    granted,
    language,
    recording_uri,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
