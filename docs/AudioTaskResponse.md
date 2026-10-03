# AudioTaskResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **string** |  | [optional] [default to undefined]
**created_at** | **string** |  | [default to undefined]
**error** | [**TaskError**](TaskError.md) |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**links** | [**ResourceLinks**](ResourceLinks.md) |  | [default to undefined]
**metadata** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**model** | **string** |  | [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Audio]
**outputs** | [**Array&lt;AudioOutput&gt;**](AudioOutput.md) |  | [optional] [default to undefined]
**routing** | [**RoutingInfo**](RoutingInfo.md) |  | [optional] [default to undefined]
**status** | **string** |  | [default to undefined]
**usage** | [**Usage**](Usage.md) |  | [optional] [default to undefined]

## Example

```typescript
import { AudioTaskResponse } from 'mm-gateway-ts';

const instance: AudioTaskResponse = {
    completed_at,
    created_at,
    error,
    id,
    links,
    metadata,
    model,
    object,
    outputs,
    routing,
    status,
    usage,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
