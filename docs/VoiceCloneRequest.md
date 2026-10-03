# VoiceCloneRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**consent** | [**VoiceConsent**](VoiceConsent.md) |  | [default to undefined]
**input** | [**Array&lt;VoiceSampleInput&gt;**](VoiceSampleInput.md) |  | [default to undefined]
**metadata** | **{ [key: string]: any; }** | Client-owned metadata returned unchanged with the task. | [optional] [default to undefined]
**model** | **string** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request\&#39;s input (modalities, dimensions, duration, ...). | [optional] [default to undefined]
**parameters** | [**VoiceParameters**](VoiceParameters.md) |  | [default to undefined]
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] [default to undefined]

## Example

```typescript
import { VoiceCloneRequest } from 'mm-gateway-ts';

const instance: VoiceCloneRequest = {
    consent,
    input,
    metadata,
    model,
    parameters,
    routing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
