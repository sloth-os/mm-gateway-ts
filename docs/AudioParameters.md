# AudioParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bitrate_kbps** | **number** |  | [optional] [default to undefined]
**delivery** | **string** |  | [optional] [default to undefined]
**file_format** | **string** |  | [optional] [default to undefined]
**instructions** | **string** |  | [optional] [default to undefined]
**language** | **string** |  | [optional] [default to undefined]
**sample_rate_hz** | **number** |  | [optional] [default to undefined]
**seed** | **number** |  | [optional] [default to undefined]
**speed** | **number** |  | [optional] [default to undefined]
**voice** | **string** | A gateway voice id from GET /v1/voices. | [optional] [default to 'default']

## Example

```typescript
import { AudioParameters } from 'mm-gateway-ts';

const instance: AudioParameters = {
    bitrate_kbps,
    delivery,
    file_format,
    instructions,
    language,
    sample_rate_hz,
    seed,
    speed,
    voice,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
