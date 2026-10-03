# AudioOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | **number** |  | [optional] [default to undefined]
**duration_seconds** | **number** |  | [optional] [default to undefined]
**mime_type** | **string** |  | [optional] [default to undefined]
**sample_rate_hz** | **number** |  | [optional] [default to undefined]
**uri** | **string** | Absolute media URI. Inline media uses a base64 data URI. | [default to undefined]

## Example

```typescript
import { AudioOutput } from 'mm-gateway-ts';

const instance: AudioOutput = {
    channels,
    duration_seconds,
    mime_type,
    sample_rate_hz,
    uri,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
