# EstimateCandidate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**admissible** | **boolean** |  | [optional] [default to true]
**estimated_cost** | **number** |  | [optional] [default to undefined]
**lifecycle** | **string** |  | [optional] [default to LifecycleEnum_Active]
**model** | **string** |  | [default to undefined]
**reason** | **string** | Why the candidate is not admissible: limits, retired, max_cost, unpriced or budget. | [optional] [default to undefined]

## Example

```typescript
import { EstimateCandidate } from 'mm-gateway-ts';

const instance: EstimateCandidate = {
    admissible,
    estimated_cost,
    lifecycle,
    model,
    reason,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
