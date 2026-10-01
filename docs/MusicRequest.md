# MusicRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**Array&lt;InputInner1&gt;**](InputInner1.md) | Non-empty ordered music-generation inputs. | [default to undefined]
**metadata** | **{ [key: string]: any; }** | Client-owned metadata returned unchanged with the task. | [optional] [default to undefined]
**model** | **string** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request\&#39;s input (modalities, dimensions, duration, ...). | [optional] [default to undefined]
**parameters** | [**MusicParameters**](MusicParameters.md) |  | [optional] [default to undefined]
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] [default to undefined]

## Example

```typescript
import { MusicRequest } from 'mm-gateway-ts';

const instance: MusicRequest = {
    input,
    metadata,
    model,
    parameters,
    routing,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
