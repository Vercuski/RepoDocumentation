# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_IEndpoint"></a> Interface IEndpoint

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Implemented by a feature slice to register its own HTTP route(s).

```csharp
public interface IEndpoint
```

## Remarks

[SliceRegistration.AddSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_AddSlices_Microsoft_Extensions_DependencyInjection_IServiceCollection_System_Reflection_Assembly_) discovers and registers implementations, and
[SliceRegistration.MapSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_MapSlices_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_) maps them, so a new slice needs no changes to <code>Program.cs</code>.

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_IEndpoint_MapEndpoint_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_"></a> MapEndpoint\(IEndpointRouteBuilder\)

Maps this slice's route(s) onto the application's routing table.

```csharp
void MapEndpoint(IEndpointRouteBuilder app)
```

#### Parameters

`app` [IEndpointRouteBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.routing.iendpointroutebuilder)

The route builder to add the endpoint(s) to.

