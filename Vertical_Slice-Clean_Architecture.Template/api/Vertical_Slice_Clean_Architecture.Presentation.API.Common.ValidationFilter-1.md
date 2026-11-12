# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_ValidationFilter_1"></a> Class ValidationFilter<TRequest\>

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Endpoint filter that validates the <code class="typeparamref">TRequest</code> argument with FluentValidation
before the route handler runs.

```csharp
public sealed class ValidationFilter<TRequest> : IEndpointFilter
```

#### Type Parameters

`TRequest` 

The request type to validate.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ValidationFilter<TRequest\>](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ValidationFilter\-1.md)

#### Implements

[IEndpointFilter](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.iendpointfilter)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_ValidationFilter_1_InvokeAsync_Microsoft_AspNetCore_Http_EndpointFilterInvocationContext_Microsoft_AspNetCore_Http_EndpointFilterDelegate_"></a> InvokeAsync\(EndpointFilterInvocationContext, EndpointFilterDelegate\)

Validates the request and either short-circuits with an error response or calls the next step in the pipeline.

```csharp
public ValueTask<object?> InvokeAsync(EndpointFilterInvocationContext context, EndpointFilterDelegate next)
```

#### Parameters

`context` [EndpointFilterInvocationContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.endpointfilterinvocationcontext)

The filter context, which holds the handler arguments and the current [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext).

`next` [EndpointFilterDelegate](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.endpointfilterdelegate)

The next filter, or the route handler itself.

#### Returns

 [ValueTask](https://learn.microsoft.com/dotnet/api/system.threading.tasks.valuetask\-1)<[object](https://learn.microsoft.com/dotnet/api/system.object)?\>

<ul><li>A <code>400 Bad Request</code> problem response if no <code class="typeparamref">TRequest</code> argument is present.</li><li>A <code>400</code> validation problem response listing the errors if validation fails.</li><li>Otherwise, the result of <code class="paramref">next</code>.</li></ul>

#### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

No `IValidator` for <code class="typeparamref">TRequest</code> is registered.

