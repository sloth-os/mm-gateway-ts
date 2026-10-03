# ManagedProxy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | [**Array&lt;ProxyAccount&gt;**](ProxyAccount.md) |  | [optional] [default to undefined]
**base_url** | **string** |  | [default to undefined]
**domain** | **string** |  | [optional] [default to undefined]
**enabled** | **boolean** |  | [optional] [default to true]
**headers** | **{ [key: string]: string; }** |  | [optional] [default to undefined]
**outbound_proxy** | **string** |  | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**timeout** | **number** |  | [optional] [default to 120]

## Example

```typescript
import { ManagedProxy } from 'mm-gateway-ts';

const instance: ManagedProxy = {
    accounts,
    base_url,
    domain,
    enabled,
    headers,
    outbound_proxy,
    tags,
    timeout,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
