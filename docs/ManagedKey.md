# ManagedKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_backends** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**allow_tags** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**budget** | [**ManagedBudget**](ManagedBudget.md) |  | [optional] [default to undefined]
**default_audio_backend** | **string** |  | [optional] [default to undefined]
**default_audio_tag** | **string** |  | [optional] [default to undefined]
**default_image_backend** | **string** |  | [optional] [default to undefined]
**default_image_tag** | **string** |  | [optional] [default to undefined]
**default_music_backend** | **string** |  | [optional] [default to undefined]
**default_music_tag** | **string** |  | [optional] [default to undefined]
**default_video_backend** | **string** |  | [optional] [default to undefined]
**default_video_tag** | **string** |  | [optional] [default to undefined]
**deny_tags** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**enabled** | **boolean** |  | [optional] [default to true]
**extra** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**id** | **string** |  | [default to undefined]
**key** | **string** |  | [default to undefined]

## Example

```typescript
import { ManagedKey } from 'mm-gateway-ts';

const instance: ManagedKey = {
    allow_backends,
    allow_tags,
    budget,
    default_audio_backend,
    default_audio_tag,
    default_image_backend,
    default_image_tag,
    default_music_backend,
    default_music_tag,
    default_video_backend,
    default_video_tag,
    deny_tags,
    enabled,
    extra,
    id,
    key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
