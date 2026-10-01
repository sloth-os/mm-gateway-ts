# BudgetState

The state of one budget (a key\'s period or a client scope).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_usd** | **number** |  | [optional] [default to undefined]
**remaining_usd** | **number** |  | [optional] [default to undefined]
**reserved_usd** | **number** |  | [optional] [default to 0.0]
**scope** | **string** |  | [optional] [default to undefined]
**spent_usd** | **number** |  | [optional] [default to 0.0]
**tasks** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { BudgetState } from 'mm-gateway-ts';

const instance: BudgetState = {
    limit_usd,
    remaining_usd,
    reserved_usd,
    scope,
    spent_usd,
    tasks,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
