# MusicTaskResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **string** |  | [optional] [default to undefined]
**created_at** | **string** |  | [default to undefined]
**error** | [**TaskError**](TaskError.md) |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**links** | [**ResourceLinks**](ResourceLinks.md) |  | [default to undefined]
**lyrics** | **string** |  | [optional] [default to undefined]
**metadata** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**model** | **string** |  | [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Music]
**outputs** | [**Array&lt;MusicOutput&gt;**](MusicOutput.md) |  | [optional] [default to undefined]
**status** | **string** |  | [default to undefined]
**usage** | [**Usage**](Usage.md) |  | [optional] [default to undefined]

## Example

```typescript
import { MusicTaskResponse } from 'mm-gateway-ts';

const instance: MusicTaskResponse = {
    completed_at,
    created_at,
    error,
    id,
    links,
    lyrics,
    metadata,
    model,
    object,
    outputs,
    status,
    usage,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
