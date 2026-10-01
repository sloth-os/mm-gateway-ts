# ModelLimitsEntry

A model catalogue entry enriched with its documented input/output limits.  ``limits`` carries the neutral limits the auto-router uses and that a client can consult when crafting a prompt for a specific model. Unknown limits are omitted; clients ignore unknown response members.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**limits** | **{ [key: string]: any; }** | Neutral input/output limits (modalities, max prompt, max output count, supported sizes/durations, role flags, ...). | [optional] [default to undefined]
**modality** | **string** |  | [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Model]

## Example

```typescript
import { ModelLimitsEntry } from 'mm-gateway-ts';

const instance: ModelLimitsEntry = {
    id,
    limits,
    modality,
    object,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
