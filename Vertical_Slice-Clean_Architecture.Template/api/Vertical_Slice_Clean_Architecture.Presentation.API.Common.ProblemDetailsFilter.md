# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_ProblemDetailsFilter"></a> Class ProblemDetailsFilter

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Endpoint filter, applied to every slice by [SliceRegistration.MapSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_MapSlices_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_), that runs the
application's [CustomizeProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.problemdetailsoptions.customizeproblemdetails) on problem bodies a slice
returns itself (for example [Problems.Conflict](Vertical_Slice_Clean_Architecture.Presentation.API.Common.Problems.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_Problems_Conflict_System_String_System_String_)).

```csharp
public sealed class ProblemDetailsFilter : IEndpointFilter
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ProblemDetailsFilter](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ProblemDetailsFilter.md)

#### Implements

[IEndpointFilter](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.iendpointfilter)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

ASP.NET Core applies [CustomizeProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.problemdetailsoptions.customizeproblemdetails) only to bodies
written through [IProblemDetailsService](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.iproblemdetailsservice) (unhandled exceptions, validation problems,
empty error status codes). A typed result such as <code>Conflict&lt;ProblemDetails&gt;</code> is serialized
directly, so without this filter it would miss members such as <code>correlationId</code>.

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_ProblemDetailsFilter_InvokeAsync_Microsoft_AspNetCore_Http_EndpointFilterInvocationContext_Microsoft_AspNetCore_Http_EndpointFilterDelegate_"></a> InvokeAsync\(EndpointFilterInvocationContext, EndpointFilterDelegate\)

Runs the slice, then customizes the [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) in its result, if any.

```csharp
public ValueTask<object?> InvokeAsync(EndpointFilterInvocationContext context, EndpointFilterDelegate next)
```

#### Parameters

`context` [EndpointFilterInvocationContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.endpointfilterinvocationcontext)

The filter context, which holds the current [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext).

`next` [EndpointFilterDelegate](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.endpointfilterdelegate)

The next filter, or the route handler itself.

#### Returns

 [ValueTask](https://learn.microsoft.com/dotnet/api/system.threading.tasks.valuetask\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)?\>

The slice's result, unchanged apart from its problem body.

