# <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware"></a> Class CorrelationIdMiddleware

Namespace: [ONIONARCH.Infrastructure.Correlation](ONIONARCH.Infrastructure.Correlation.md)  
Assembly: ONIONARCH.Infrastructure.dll  

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

```csharp
public sealed class CorrelationIdMiddleware
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CorrelationIdMiddleware](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Reuses the caller's [CorrelationIdMiddleware.HeaderName](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md#ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName) header when present, otherwise generates a new GUID.
The ID is stored in [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md), echoed back on the response header, and
pushed as a <code>CorrelationId</code> logging scope for the rest of the pipeline. Register it (via
<code>UseCorrelationIdMiddleware()</code>) before <code>UseExceptionHandler()</code> so exception responses
can include the ID.

## Constructors

### <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware__ctor_Microsoft_AspNetCore_Http_RequestDelegate_"></a> CorrelationIdMiddleware\(RequestDelegate\)

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

```csharp
public CorrelationIdMiddleware(RequestDelegate next)
```

#### Parameters

`next` [RequestDelegate](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.requestdelegate)

The next middleware in the pipeline.

#### Remarks

Reuses the caller's [CorrelationIdMiddleware.HeaderName](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md#ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName) header when present, otherwise generates a new GUID.
The ID is stored in [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md), echoed back on the response header, and
pushed as a <code>CorrelationId</code> logging scope for the rest of the pipeline. Register it (via
<code>UseCorrelationIdMiddleware()</code>) before <code>UseExceptionHandler()</code> so exception responses
can include the ID.

## Fields

### <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware_HeaderName"></a> HeaderName

The HTTP header used to receive and return the correlation ID.

```csharp
public const string HeaderName = "X-Correlation-Id"
```

#### Field Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware_InvokeAsync_Microsoft_AspNetCore_Http_HttpContext_ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor_Microsoft_Extensions_Logging_ILogger_ONIONARCH_Infrastructure_Correlation_CorrelationIdMiddleware__"></a> InvokeAsync\(HttpContext, CorrelationIdAccessor, ILogger<CorrelationIdMiddleware\>\)

Resolves the correlation ID for the current request and invokes the rest of the pipeline
inside a logging scope that carries it.

```csharp
public Task InvokeAsync(HttpContext context, CorrelationIdAccessor accessor, ILogger<CorrelationIdMiddleware> logger)
```

#### Parameters

`context` [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext)

The current HTTP context.

`accessor` [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md)

The ambient correlation ID store (method-injected per request).

`logger` [ILogger](https://learn.microsoft.com/dotnet/api/microsoft.extensions.logging.ilogger\-1)<[CorrelationIdMiddleware](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md)\>

The logger used to open the correlation ID scope.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the rest of the pipeline has finished.

