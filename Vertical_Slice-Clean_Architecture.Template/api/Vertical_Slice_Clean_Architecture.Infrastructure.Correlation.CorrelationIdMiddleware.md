# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware"></a> Class CorrelationIdMiddleware

Namespace: [Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Infrastructure.dll  

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

```csharp
public sealed class CorrelationIdMiddleware
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CorrelationIdMiddleware](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
Reuses the caller's [CorrelationIdMiddleware.HeaderName](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md#Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName) header when it is a well-formed ID (see
[CorrelationIdMiddleware.IsValid](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md#Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_IsValid_System_String_)), otherwise generates a new GUID. The ID is stored in
[CorrelationIdAccessor](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md), echoed back on the response header, added as a
<code>correlation.id</code> tag on the current trace activity, and pushed as a <code>CorrelationId</code>
logging scope for the rest of the pipeline.
</p>
<p>
Register it (via <code>UseCorrelationIdMiddleware()</code>) first in the pipeline, before
<code>UseExceptionHandler()</code>, so error responses and their log entries carry the ID.
</p>

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware__ctor_Microsoft_AspNetCore_Http_RequestDelegate_"></a> CorrelationIdMiddleware\(RequestDelegate\)

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

```csharp
public CorrelationIdMiddleware(RequestDelegate next)
```

#### Parameters

`next` [RequestDelegate](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.requestdelegate)

The next middleware in the pipeline.

#### Remarks

<p>
Reuses the caller's [CorrelationIdMiddleware.HeaderName](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md#Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName) header when it is a well-formed ID (see
[CorrelationIdMiddleware.IsValid](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md#Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_IsValid_System_String_)), otherwise generates a new GUID. The ID is stored in
[CorrelationIdAccessor](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md), echoed back on the response header, added as a
<code>correlation.id</code> tag on the current trace activity, and pushed as a <code>CorrelationId</code>
logging scope for the rest of the pipeline.
</p>
<p>
Register it (via <code>UseCorrelationIdMiddleware()</code>) first in the pipeline, before
<code>UseExceptionHandler()</code>, so error responses and their log entries carry the ID.
</p>

## Fields

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName"></a> HeaderName

The HTTP header used to receive and return the correlation ID.

```csharp
public const string HeaderName = "X-Correlation-Id"
```

#### Field Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_MaxLength"></a> MaxLength

The longest incoming correlation ID that is accepted.

```csharp
public const int MaxLength = 64
```

#### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_InvokeAsync_Microsoft_AspNetCore_Http_HttpContext_Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdAccessor_Microsoft_Extensions_Logging_ILogger_Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware__"></a> InvokeAsync\(HttpContext, CorrelationIdAccessor, ILogger<CorrelationIdMiddleware\>\)

Resolves the correlation ID for the current request and invokes the rest of the pipeline
inside a logging scope that carries it.

```csharp
public Task InvokeAsync(HttpContext context, CorrelationIdAccessor accessor, ILogger<CorrelationIdMiddleware> logger)
```

#### Parameters

`context` [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext)

The current HTTP context.

`accessor` [CorrelationIdAccessor](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md)

The ambient correlation ID store (method-injected per request).

`logger` [ILogger](https://learn.microsoft.com/dotnet/api/microsoft.extensions.logging.ilogger\-1)<[CorrelationIdMiddleware](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md)\>

The logger used to open the correlation ID scope.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the rest of the pipeline has finished.

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_IsValid_System_String_"></a> IsValid\(string?\)

Determines whether a caller-supplied correlation ID can be reused. The value is echoed in a
response header and written to logs, so only short values of plain ID characters are
accepted; anything else (including several header values joined by commas) is replaced.

```csharp
public static bool IsValid(string? value)
```

#### Parameters

`value` [string](https://learn.microsoft.com/dotnet/api/system.string)?

The incoming header value.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if <code class="paramref">value</code> is 1 to [CorrelationIdMiddleware.MaxLength](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md#Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdMiddleware_MaxLength) allowed characters.

