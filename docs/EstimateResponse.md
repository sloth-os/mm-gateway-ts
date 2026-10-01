# EstimateResponse

The routing and cost a create would get, without creating a task.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | [**BudgetState**](BudgetState.md) |  | [optional] [default to undefined]
**candidates** | [**Array&lt;EstimateCandidate&gt;**](EstimateCandidate.md) |  | [optional] [default to undefined]
**currency** | **string** |  | [optional] [default to CurrencyEnum_Usd]
**estimated_cost** | **number** |  | [optional] [default to undefined]
**modality** | **string** |  | [default to undefined]
**model** | **string** |  | [optional] [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Estimate]

## Example

```typescript
import { EstimateResponse } from 'mm-gateway-ts';

const instance: EstimateResponse = {
    budget,
    candidates,
    currency,
    estimated_cost,
    modality,
    model,
    object,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
