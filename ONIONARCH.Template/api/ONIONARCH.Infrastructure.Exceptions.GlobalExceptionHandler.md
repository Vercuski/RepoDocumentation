# <a id="ONIONARCH_Infrastructure_Exceptions_GlobalExceptionHandler"></a> Class GlobalExceptionHandler

Namespace: [ONIONARCH.Infrastructure.Exceptions](ONIONARCH.Infrastructure.Exceptions.md)  
Assembly: ONIONARCH.Infrastructure.dll  

Centralized handler for unhandled exceptions in every web host. Logs the exception and
returns an RFC 7807 [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) 500 response that includes the request's
correlation ID, without leaking exception details to the caller.

```csharp
public sealed class GlobalExceptionHandler : IExceptionHandler
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GlobalExceptionHandler](ONIONARCH.Infrastructure.Exceptions.GlobalExceptionHandler.md)

#### Implements

[IExceptionHandler](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.diagnostics.iexceptionhandler)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Register with <code>AddExceptionHandler&lt;GlobalExceptionHandler&gt;()</code> and enable with
<code>UseExceptionHandler()</code>.

## Constructors

### <a id="ONIONARCH_Infrastructure_Exceptions_GlobalExceptionHandler__ctor_Microsoft_Extensions_Logging_ILogger_ONIONARCH_Infrastructure_Exceptions_GlobalExceptionHandler__ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor_"></a> GlobalExceptionHandler\(ILogger<GlobalExceptionHandler\>, CorrelationIdAccessor\)

Centralized handler for unhandled exceptions in every web host. Logs the exception and
returns an RFC 7807 [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) 500 response that includes the request's
correlation ID, without leaking exception details to the caller.

```csharp
public GlobalExceptionHandler(ILogger<GlobalExceptionHandler> logger, CorrelationIdAccessor correlationIdAccessor)
```

#### Parameters

`logger` [ILogger](https://learn.microsoft.com/dotnet/api/microsoft.extensions.logging.ilogger\-1)<[GlobalExceptionHandler](ONIONARCH.Infrastructure.Exceptions.GlobalExceptionHandler.md)\>

The logger used to record the exception.

`correlationIdAccessor` [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md)

Supplies the current request's correlation ID.

#### Remarks

Register with <code>AddExceptionHandler&lt;GlobalExceptionHandler&gt;()</code> and enable with
<code>UseExceptionHandler()</code>.

## Methods

### <a id="ONIONARCH_Infrastructure_Exceptions_GlobalExceptionHandler_TryHandleAsync_Microsoft_AspNetCore_Http_HttpContext_System_Exception_System_Threading_CancellationToken_"></a> TryHandleAsync\(HttpContext, Exception, CancellationToken\)

Logs <code class="paramref">exception</code> and writes a 500 problem details response carrying a
<code>correlationId</code> extension member.

```csharp
public ValueTask<bool> TryHandleAsync(HttpContext httpContext, Exception exception, CancellationToken cancellationToken)
```

#### Parameters

`httpContext` [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext)

The HTTP context of the failed request.

`exception` [Exception](https://learn.microsoft.com/dotnet/api/system.exception)

The unhandled exception.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel writing the response.

#### Returns

 [ValueTask](https://learn.microsoft.com/dotnet/api/system.threading.tasks.valuetask\-1)<[bool](https://learn.microsoft.com/dotnet/api/system.boolean)\>

Always <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>, indicating the exception has been handled.

