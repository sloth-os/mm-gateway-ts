# Usage

Provider-neutral usage fields shared by all three modalities.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost** | **number** |  | [optional] [default to undefined]
**duration_seconds** | **number** |  | [optional] [default to undefined]
**input_tokens** | **number** |  | [optional] [default to undefined]
**output_count** | **number** |  | [optional] [default to undefined]
**output_tokens** | **number** |  | [optional] [default to undefined]
**total_tokens** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { Usage } from 'mm-gateway-ts';

const instance: Usage = {
    cost,
    duration_seconds,
    input_tokens,
    output_count,
    output_tokens,
    total_tokens,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
