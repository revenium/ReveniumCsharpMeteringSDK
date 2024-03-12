# IO.Swagger.io.revenium.MeteringRequestDTO
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Api** | **string** |  | [optional] 
**ProductKey** | **string** | The Product Key ID | [optional] 
**Application** | **string** | The Application ID | [optional] 
**Method** | **string** | The HTTP method being invoked | 
**Url** | **string** | The HTTP URL being invoked | [optional] 
**Metadata** | **string** | Additional billing metadata (supports numeric values and comma-seperated key-value pairs) | [optional] 
**BackendLatency** | **double?** | Backend API response time | [optional] 
**GatewayLatency** | **double?** | Latency introduced by the API GW | [optional] 
**ResponseCode** | **int?** | Backend HTTP response code | 
**TimedOut** | **bool?** | Whether or not the backend timed out | [optional] 
**RequestMessageSize** | **long?** | The size of the API request in bytes | [optional] 
**ResponseMessageSize** | **long?** | The size of the API response in bytes | [optional] 
**RequestHeaders** | **List&lt;string&gt;** | The comma seperated list of names of the headers in the request | 
**ResponseHeaders** | **List&lt;string&gt;** | The comma seperated list of names of the headers in the response | 
**UserAgent** | **string** | The HTTP User Agent | [optional] 
**RemoteUser** | **string** | The Remote User | [optional] 
**RemoteHost** | **string** | The Remote Host | [optional] 
**HttpProtocol** | **string** | The HTTP Protocol | [optional] 
**ContentType** | **string** | The Content Type | [optional] 
**CorrelationId** | **string** | The Correlation ID | [optional] 
**PlatformAPIKey** | **string** | platformAPIKey | 
**Elements** | [**List&lt;ElementDTO&gt;**](ElementDTO.md) | Dynamic metering elements | 
**Source** | **string** | the source of the event | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

