# RoutingInfo

How auto mode served a task (docs/design/auto-mode.md#fallbacks).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **number** |  | [optional] [default to 1]
**budget** | [**BudgetState**](BudgetState.md) |  | [optional] [default to undefined]
**estimated_cost** | **number** |  | [optional] [default to undefined]
**fallback** | **boolean** |  | [optional] [default to false]
**fallback_reason** | **string** |  | [optional] [default to undefined]
**optimize** | **string** |  | [optional] [default to 'balanced']
**requested_model** | **string** |  | [default to undefined]

## Example

```typescript
import { RoutingInfo } from 'mm-gateway-ts';

const instance: RoutingInfo = {
    attempts,
    budget,
    estimated_cost,
    fallback,
    fallback_reason,
    optimize,
    requested_model,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
