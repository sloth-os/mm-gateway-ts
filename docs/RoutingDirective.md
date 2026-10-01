# RoutingDirective

Select a server-defined, provider-neutral routing policy.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile** | **string** | Gateway-defined routing profile, such as &#x60;quality&#x60;, &#x60;fast&#x60;, or &#x60;eu&#x60;. It never names a provider or backend. | [default to undefined]

## Example

```typescript
import { RoutingDirective } from 'mm-gateway-ts';

const instance: RoutingDirective = {
    profile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
