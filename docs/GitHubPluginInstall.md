# GitHubPluginInstall


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_options** | [**PluginOptions**](PluginOptions.md) |  | [optional] [default to undefined]
**ref** | **string** | Branch, tag or commit to fetch. | [optional] [default to 'HEAD']
**repository** | **string** | HTTPS GitHub repository URL. | [default to undefined]
**subdirectory** | **string** |  | [optional] [default to '']

## Example

```typescript
import { GitHubPluginInstall } from 'mm-gateway-ts';

const instance: GitHubPluginInstall = {
    _options,
    ref,
    repository,
    subdirectory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
