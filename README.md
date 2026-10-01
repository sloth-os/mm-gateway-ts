## mm-gateway-ts@0.1.0

This generator creates TypeScript/JavaScript client that utilizes [axios](https://github.com/axios/axios). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition will be automatically resolved via `package.json`. ([Reference](https://www.typescriptlang.org/docs/handbook/declaration-files/consumption.html))

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```

### Publishing

First build the package then run `npm publish`

### Consuming

navigate to the folder of your consuming project and run one of the following commands.

_published:_

```
npm install mm-gateway-ts@0.1.0 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ImagesApi* | [**createImage**](docs/ImagesApi.md#createimage) | **POST** /v1/images | Create an image task
*ImagesApi* | [**getImage**](docs/ImagesApi.md#getimage) | **GET** /v1/images/{image_id} | Retrieve an image task
*MetaApi* | [**getHealth**](docs/MetaApi.md#gethealth) | **GET** /health | Health
*MetaApi* | [**getMetrics**](docs/MetaApi.md#getmetrics) | **GET** /metrics | Metrics
*MetaApi* | [**listModelLimits**](docs/MetaApi.md#listmodellimits) | **GET** /v1/models/limits | List Model Limits
*MetaApi* | [**listModels**](docs/MetaApi.md#listmodels) | **GET** /v1/models | List Models
*MusicApi* | [**createMusic**](docs/MusicApi.md#createmusic) | **POST** /v1/music | Create a music task
*MusicApi* | [**getMusic**](docs/MusicApi.md#getmusic) | **GET** /v1/music/{music_id} | Retrieve a music task
*ProxyApi* | [**proxyRequestDelete**](docs/ProxyApi.md#proxyrequestdelete) | **DELETE** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestGet**](docs/ProxyApi.md#proxyrequestget) | **GET** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestHead**](docs/ProxyApi.md#proxyrequesthead) | **HEAD** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestOptions**](docs/ProxyApi.md#proxyrequestoptions) | **OPTIONS** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestPatch**](docs/ProxyApi.md#proxyrequestpatch) | **PATCH** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestPost**](docs/ProxyApi.md#proxyrequestpost) | **POST** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*ProxyApi* | [**proxyRequestPut**](docs/ProxyApi.md#proxyrequestput) | **PUT** /proxy/{domain}/{path} | Forward a request through a domain-matched proxy
*VideosApi* | [**createVideo**](docs/VideosApi.md#createvideo) | **POST** /v1/videos | Create a video task
*VideosApi* | [**getVideo**](docs/VideosApi.md#getvideo) | **GET** /v1/videos/{video_id} | Retrieve a video task


### Documentation For Models

 - [Dimensions](docs/Dimensions.md)
 - [HealthResponse](docs/HealthResponse.md)
 - [ImageInput](docs/ImageInput.md)
 - [ImageOutput](docs/ImageOutput.md)
 - [ImageParameters](docs/ImageParameters.md)
 - [ImageRequest](docs/ImageRequest.md)
 - [ImageTaskResponse](docs/ImageTaskResponse.md)
 - [InputInner](docs/InputInner.md)
 - [InputInner1](docs/InputInner1.md)
 - [InputInner2](docs/InputInner2.md)
 - [LyricsInput](docs/LyricsInput.md)
 - [ModelEntry](docs/ModelEntry.md)
 - [ModelLimitsEntry](docs/ModelLimitsEntry.md)
 - [ModelLimitsListResponse](docs/ModelLimitsListResponse.md)
 - [ModelListResponse](docs/ModelListResponse.md)
 - [MusicAudioInput](docs/MusicAudioInput.md)
 - [MusicImageInput](docs/MusicImageInput.md)
 - [MusicOutput](docs/MusicOutput.md)
 - [MusicParameters](docs/MusicParameters.md)
 - [MusicRequest](docs/MusicRequest.md)
 - [MusicTaskResponse](docs/MusicTaskResponse.md)
 - [ProblemDetail](docs/ProblemDetail.md)
 - [ResourceLinks](docs/ResourceLinks.md)
 - [RoutingDirective](docs/RoutingDirective.md)
 - [TaskError](docs/TaskError.md)
 - [TextInput](docs/TextInput.md)
 - [Usage](docs/Usage.md)
 - [VideoAudioInput](docs/VideoAudioInput.md)
 - [VideoImageInput](docs/VideoImageInput.md)
 - [VideoInput](docs/VideoInput.md)
 - [VideoOutput](docs/VideoOutput.md)
 - [VideoParameters](docs/VideoParameters.md)
 - [VideoRequest](docs/VideoRequest.md)
 - [VideoTaskResponse](docs/VideoTaskResponse.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="BearerAuth"></a>
### BearerAuth

- **Type**: Bearer authentication (API key)

