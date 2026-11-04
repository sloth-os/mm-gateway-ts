# RoutingAdjustment

What the backend that served a task could not carry as asked (docs/design/unification.md#best-effort).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **string** |  | [default to undefined]
**detail** | **string** |  | [optional] [default to undefined]
**parameter** | **string** |  | [default to undefined]

## Example

```typescript
import { RoutingAdjustment } from 'mm-gateway-ts';

const instance: RoutingAdjustment = {
    action,
    detail,
    parameter,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
