# BudgetDirective

A client-chosen spend bucket within the key, optionally self-capped.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit_usd** | **number** | Self-imposed cap for the scope in USD (the operator\&#39;s scope cap still applies). | [optional] [default to undefined]
**scope** | **string** | Spend bucket name (a project, a customer, a batch). | [default to undefined]

## Example

```typescript
import { BudgetDirective } from 'mm-gateway-ts';

const instance: BudgetDirective = {
    limit_usd,
    scope,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
