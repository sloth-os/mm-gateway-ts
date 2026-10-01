# UsageResponse

Spend, reservations and budgets of the authenticated key.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] [default to CurrencyEnum_Usd]
**key** | [**BudgetState**](BudgetState.md) |  | [default to undefined]
**models** | [**Array&lt;ModelSpend&gt;**](ModelSpend.md) |  | [optional] [default to undefined]
**object** | **string** |  | [optional] [default to ObjectEnum_Usage]
**period** | [**UsagePeriod**](UsagePeriod.md) |  | [default to undefined]
**scopes** | [**Array&lt;BudgetState&gt;**](BudgetState.md) |  | [optional] [default to undefined]

## Example

```typescript
import { UsageResponse } from 'mm-gateway-ts';

const instance: UsageResponse = {
    currency,
    key,
    models,
    object,
    period,
    scopes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
