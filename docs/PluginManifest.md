# PluginManifest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_version** | **string** |  | [optional] [default to ApiVersionEnum__1]
**author** | **string** |  | [optional] [default to '']
**backend_types** | **Array&lt;string&gt;** | Backend types for automatic authentication hooks; * matches all. | [optional] [default to undefined]
**default_config** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to '']
**homepage** | **string** |  | [optional] [default to undefined]
**hooks** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**methods** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**name** | **string** |  | [default to undefined]
**paths** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**providers** | **Array&lt;string&gt;** | New provider types exported by this plugin. | [optional] [default to undefined]
**response_body** | **string** |  | [optional] [default to ResponseBodyEnum_None]
**version** | **string** |  | [default to undefined]

## Example

```typescript
import { PluginManifest } from 'mm-gateway-ts';

const instance: PluginManifest = {
    api_version,
    author,
    backend_types,
    default_config,
    description,
    homepage,
    hooks,
    id,
    methods,
    name,
    paths,
    providers,
    response_body,
    version,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
