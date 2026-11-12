# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Endpoint"></a> Class GetSample.Endpoint

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Registers the <code>GET /Sample/{Id:guid}</code> route for this slice.

```csharp
public sealed class GetSample.Endpoint : IEndpoint
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSample.Endpoint](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Endpoint.md)

#### Implements

[IEndpoint](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.IEndpoint.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Endpoint_MapEndpoint_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_"></a> MapEndpoint\(IEndpointRouteBuilder\)

Maps <code>GET /Sample/{Id:guid}</code> to [GetSample.Handler.Handle](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.GetSample.Handler.md#Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Handler_Handle_Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Query_System_Threading_CancellationToken_). The route is named <code>GetSample</code> and tagged <code>Sample</code> in OpenAPI.

```csharp
public void MapEndpoint(IEndpointRouteBuilder app)
```

#### Parameters

`app` [IEndpointRouteBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.routing.iendpointroutebuilder)

The route builder to add the endpoint to.

