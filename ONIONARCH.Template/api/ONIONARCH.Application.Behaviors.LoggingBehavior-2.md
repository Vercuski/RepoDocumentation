# <a id="ONIONARCH_Application_Behaviors_LoggingBehavior_2"></a> Class LoggingBehavior<TRequest, TResponse\>

Namespace: [ONIONARCH.Application.Behaviors](ONIONARCH.Application.Behaviors.md)  
Assembly: ONIONARCH.Application.dll  

Logs entry, successful completion, and failure of every command/query. Combined with
the ambient correlation-ID logging scope pushed by CorrelationIdMiddleware (Infrastructure),
this reconstructs the full "path" of a request through the CQRS pipeline without any handler
needing to know a correlation ID exists.

```csharp
public sealed class LoggingBehavior<TRequest, TResponse> : IPipelineBehavior<TRequest, TResponse> where TRequest : IAppRequest<TResponse>
```

#### Type Parameters

`TRequest` 

The request type being dispatched.

`TResponse` 

The response type produced by the request's handler.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[LoggingBehavior<TRequest, TResponse\>](ONIONARCH.Application.Behaviors.LoggingBehavior\-2.md)

#### Implements

[IPipelineBehavior<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IPipelineBehavior\-2.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Behaviors_LoggingBehavior_2__ctor_Microsoft_Extensions_Logging_ILogger_ONIONARCH_Application_Behaviors_LoggingBehavior__0__1___"></a> LoggingBehavior\(ILogger<LoggingBehavior<TRequest, TResponse\>\>\)

Logs entry, successful completion, and failure of every command/query. Combined with
the ambient correlation-ID logging scope pushed by CorrelationIdMiddleware (Infrastructure),
this reconstructs the full "path" of a request through the CQRS pipeline without any handler
needing to know a correlation ID exists.

```csharp
public LoggingBehavior(ILogger<LoggingBehavior<TRequest, TResponse>> logger)
```

#### Parameters

`logger` [ILogger](https://learn.microsoft.com/dotnet/api/microsoft.extensions.logging.ilogger\-1)<[LoggingBehavior](ONIONARCH.Application.Behaviors.LoggingBehavior\-2.md)<TRequest, TResponse\>\>

The logger used to write pipeline entries.

## Methods

### <a id="ONIONARCH_Application_Behaviors_LoggingBehavior_2_Handle__0_System_Func_System_Threading_Tasks_Task__1___System_Threading_CancellationToken_"></a> Handle\(TRequest, Func<Task<TResponse\>\>, CancellationToken\)

Logs the request name before and after invoking <code class="paramref">next</code>. Exceptions are
logged at error level and rethrown unchanged so the global exception handler still sees them.

```csharp
public Task<TResponse> Handle(TRequest request, Func<Task<TResponse>> next, CancellationToken cancellationToken)
```

#### Parameters

`request` TRequest

The request being dispatched.

`next` [Func](https://learn.microsoft.com/dotnet/api/system.func\-1)<[Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>\>

Invokes the rest of the pipeline.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>

The response produced by <code class="paramref">next</code>.

