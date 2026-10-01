# RoutingDirective

Steer auto mode: policy, ordering, cost ceiling, fallbacks and budget scope.  See docs/design/auto-mode.md. Every member is optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | [**BudgetDirective**](BudgetDirective.md) |  | [optional] [default to undefined]
**fallback** | **string** | Pinned models only: &#x60;none&#x60; (default) tries one backend, &#x60;same_model&#x60; every backend/account serving the model, &#x60;any&#x60; also the replacement and the auto candidates when the model is retired or unavailable. | [optional] [default to undefined]
**max_cost_usd** | **number** | Hard per-task ceiling on the estimated cost in USD; unpriced models are excluded. | [optional] [default to undefined]
**optimize** | **string** | How admissible candidates are ordered (default: the gateway\&#39;s default, &#x60;balanced&#x60;). | [optional] [default to undefined]
**profile** | **string** | Gateway-defined routing profile, such as &#x60;quality&#x60;, &#x60;fast&#x60;, or &#x60;eu&#x60;. It never names a provider or backend. | [optional] [default to undefined]

## Example

```typescript
import { RoutingDirective } from 'mm-gateway-ts';

const instance: RoutingDirective = {
    budget,
    fallback,
    max_cost_usd,
    optimize,
    profile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
