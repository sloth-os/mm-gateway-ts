# VoiceResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **string** |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**error** | [**TaskError**](TaskError.md) |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**kind** | **string** |  | [optional] [default to KindEnum_Cloned]
**links** | [**ResourceLinks**](ResourceLinks.md) |  | [default to undefined]
**metadata** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**model** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Voice]
**routing** | [**RoutingInfo**](RoutingInfo.md) |  | [optional] [default to undefined]
**status** | **string** |  | [default to undefined]
**usage** | [**Usage**](Usage.md) |  | [optional] [default to undefined]
**verification_required** | **boolean** |  | [optional] [default to false]

## Example

```typescript
import { VoiceResponse } from 'mm-gateway-ts';

const instance: VoiceResponse = {
    completed_at,
    created_at,
    error,
    id,
    kind,
    links,
    metadata,
    model,
    name,
    object,
    routing,
    status,
    usage,
    verification_required,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
