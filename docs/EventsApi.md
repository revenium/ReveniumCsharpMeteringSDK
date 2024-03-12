# IO.Swagger.io.revenium.EventsApi

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**SaveEvent**](EventsApi.md#saveevent) | **POST** /event | Save can API event

<a name="saveevent"></a>
# **SaveEvent**
> void SaveEvent (ApiEventDTO body)

Save can API event

Save an API event

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.io.revenium;
using IO.Swagger.Client;
using IO.Swagger.io.revenium;

namespace Example
{
    public class SaveEventExample
    {
        public void main()
        {
            var apiInstance = new EventsApi();
            var body = new ApiEventDTO(); // ApiEventDTO | 

            try
            {
                // Save can API event
                apiInstance.SaveEvent(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EventsApi.SaveEvent: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ApiEventDTO**](ApiEventDTO.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
