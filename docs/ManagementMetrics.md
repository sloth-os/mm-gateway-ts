# ManagementMetrics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collected_at** | **string** |  | [default to undefined]
**counters** | [**Array&lt;CounterSample&gt;**](CounterSample.md) |  | [default to undefined]
**enabled** | **boolean** |  | [default to undefined]
**histograms** | [**Array&lt;HistogramSample&gt;**](HistogramSample.md) |  | [default to undefined]
**selection** | [**Array&lt;SelectionHealth&gt;**](SelectionHealth.md) |  | [default to undefined]

## Example

```typescript
import { ManagementMetrics } from 'mm-gateway-ts';

const instance: ManagementMetrics = {
    collected_at,
    counters,
    enabled,
    histograms,
    selection,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
