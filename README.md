# IO.Swagger - ASP.NET Core 2.0 Server

Revenium Metering API

## Clone Repository

```
git clone repo_address
```

## Build Project 
Right Click on the sln file and select build 

note where the dll file is built 
```
ie. src\IO.Swagger\bin\Debug\net6.0\IO.Revenium.dll
```


## Add to Project 
Right click on dependencies file and add ProjectReference
Select the IO.Revenium.dll files.

## Add Dependencies for SDK
Add Nuget Packages for SDK to function 
* the version specified or later 
```
Newtonsoft.JSON (13.0.3)
Swashbuckle.AspNetCore (6.5.0)
Swashbuckle.AspNetCore.Annotations (6.5.0)
```
## Example implementation of SDK 

```c#
using IO.Revenium.Controllers;
using IO.Revenium.Models;
 class Hello
{
    static void Main(string[] args)
    {
        
        //Make a Metering Request to Revenium
        MeteringRequestDTO requestDTO = new MeteringRequestDTO();
        requestDTO.Method = "GET";
        requestDTO.PlatformAPIKey = "test_key";
        requestDTO.Url = "api/1";
        requestDTO.Application = "77273cd5-02be-46da-8022-87e237f25393";
        requestDTO.ResponseCode = 200;
        requestDTO.RequestHeaders = new List<string> { };
        requestDTO.ResponseHeaders = new List<string> { };
        requestDTO.Metadata = "test";
        //optional
        requestDTO.BackendLatency = 100.0;
        requestDTO.GatewayLatency = 10.0;
        requestDTO.TimedOut = false;
        requestDTO.RequestMessageSize = 1024;
        requestDTO.ResponseMessageSize = 1024;
        requestDTO.RemoteUser = "example@gmail.com";
        requestDTO.CorrelationId = "77273cd5-02be-46da-8022-87e237f25393";
        requestDTO.HttpProtocol = "https";


        MetringApiController controller = new MetringApiController();
        try
        {
           var result = controller.Meter(requestDTO);
            Console.WriteLine(result);
        }catch (Exception ex)
        {
            Console.WriteLine(ex.ToString());
        }
       

        //Create a new API event in Revenium
        ApiEventDTO eventDTO = new ApiEventDTO();
        eventDTO.ResponseCode = 201;
        eventDTO.RequestId = "test";
        eventDTO.EventType = ApiEventDTO.EventTypeEnum.RESPONSEEnum;
        //second event type
       // eventDTO.EventType = ApiEventDTO.EventTypeEnum.REQUESTEnum;

        EventsApiController eventsApiController = new EventsApiController();
        try
        {
            var result = eventsApiController.SaveEvent(eventDTO);
            Console.WriteLine(result);
        }
        catch (Exception ex)
        {
            Console.WriteLine(ex.ToString());
        }


    }
}
```
