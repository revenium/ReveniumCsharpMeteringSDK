# IO.Swagger.io.revenium.MetringApi

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Meter**](MetringApi.md#meter) | **POST** /meter | Insert API metering data
[**Valid**](MetringApi.md#valid) | **GET** /meter/product-key | Determine if a ProductKey is valid or not

<a name="meter"></a>
# **Meter**
> Unit Meter (MeteringRequestDTO body)

Insert API metering data

Insert API metering data

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.io.revenium;
using IO.Swagger.Client;
using IO.Swagger.io.revenium;

namespace Example
{
    public class MeterExample
    {
        public void main()
        {
            var apiInstance = new MetringApi();
            var body = new MeteringRequestDTO(); // MeteringRequestDTO | 

            try
            {
                // Insert API metering data
                Unit result = apiInstance.Meter(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling MetringApi.Meter: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**MeteringRequestDTO**](MeteringRequestDTO.md)|  | 

### Return type

[**Unit**](Unit.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="valid"></a>
# **Valid**
> Object Valid (string productKey = null, string application = null)

Determine if a ProductKey is valid or not

Determine if a ProductKey is valid or not

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.io.revenium;
using IO.Swagger.Client;
using IO.Swagger.io.revenium;

namespace Example
{
    public class ValidExample
    {
        public void main()
        {
            var apiInstance = new MetringApi();
            var productKey = productKey_example;  // string | The product key (optional) 
            var application = application_example;  // string | The application ID (optional) 

            try
            {
                // Determine if a ProductKey is valid or not
                Object result = apiInstance.Valid(productKey, application);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling MetringApi.Valid: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productKey** | **string**| The product key | [optional] 
 **application** | **string**| The application ID | [optional] 

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
