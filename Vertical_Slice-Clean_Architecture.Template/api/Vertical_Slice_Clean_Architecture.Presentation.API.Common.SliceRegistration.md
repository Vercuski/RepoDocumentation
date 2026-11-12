# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration"></a> Class SliceRegistration

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Extension methods that discover, register and map vertical slices by assembly scanning.

```csharp
public static class SliceRegistration
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SliceRegistration](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.SliceRegistration.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_AddSlices_Microsoft_Extensions_DependencyInjection_IServiceCollection_System_Reflection_Assembly_"></a> AddSlices\(IServiceCollection, Assembly\)

Scans <code class="paramref">assembly</code> and registers every slice component it finds.

```csharp
public static IServiceCollection AddSlices(this IServiceCollection services, Assembly assembly)
```

#### Parameters

`services` [IServiceCollection](https://learn.microsoft.com/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection)

The service collection to add registrations to.

`assembly` [Assembly](https://learn.microsoft.com/dotnet/api/system.reflection.assembly)

The assembly to scan, usually the API assembly.

#### Returns

 [IServiceCollection](https://learn.microsoft.com/dotnet/api/microsoft.extensions.dependencyinjection.iservicecollection)

The same <code class="paramref">services</code> instance, for chaining.

#### Remarks

Only concrete, non-generic classes are considered:

<ul><li>Each [ISliceHandler](Vertical_Slice_Clean_Architecture.Presentation.API.Common.ISliceHandler.md) is registered as a scoped service under its concrete type.</li><li>Each [IEndpoint](Vertical_Slice_Clean_Architecture.Presentation.API.Common.IEndpoint.md) is registered as a singleton [IEndpoint](Vertical_Slice_Clean_Architecture.Presentation.API.Common.IEndpoint.md). <code>TryAddEnumerable</code> prevents duplicates if this method is called more than once.</li><li>All FluentValidation validators, including internal ones, are registered.</li></ul>

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_MapSlices_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_"></a> MapSlices\(IEndpointRouteBuilder\)

Resolves every registered [IEndpoint](Vertical_Slice_Clean_Architecture.Presentation.API.Common.IEndpoint.md) and calls [IEndpoint.MapEndpoint](Vertical_Slice_Clean_Architecture.Presentation.API.Common.IEndpoint.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_IEndpoint_MapEndpoint_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_) on it.

```csharp
public static IEndpointRouteBuilder MapSlices(this IEndpointRouteBuilder app)
```

#### Parameters

`app` [IEndpointRouteBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.routing.iendpointroutebuilder)

The route builder (typically the <code>WebApplication</code>) to map routes onto.

#### Returns

 [IEndpointRouteBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.routing.iendpointroutebuilder)

The same <code class="paramref">app</code> instance, for chaining.

#### Remarks

Call this after the application is built and after [SliceRegistration.AddSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_AddSlices_Microsoft_Extensions_DependencyInjection_IServiceCollection_System_Reflection_Assembly_) has run.

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_WithValidation__1_Microsoft_AspNetCore_Builder_RouteHandlerBuilder_"></a> WithValidation<TRequest\>\(RouteHandlerBuilder\)

Adds FluentValidation of the <code class="typeparamref">TRequest</code> argument to a route, and declares
in OpenAPI that the route can return a validation problem response.

```csharp
public static RouteHandlerBuilder WithValidation<TRequest>(this RouteHandlerBuilder builder)
```

#### Parameters

`builder` [RouteHandlerBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.routehandlerbuilder)

The route handler builder to add the filter to.

#### Returns

 [RouteHandlerBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.routehandlerbuilder)

The same <code class="paramref">builder</code> instance, for chaining.

#### Type Parameters

`TRequest` 

The request type to validate. An `IValidator` for it must be registered.

