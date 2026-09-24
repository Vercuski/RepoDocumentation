# <a id="ONIONARCH_Presentation_Console_Worker"></a> Class Worker

Namespace: [ONIONARCH.Presentation.Console](ONIONARCH.Presentation.Console.md)  
Assembly: ONIONARCH.Presentation.Console.dll  

Sample background worker for the console host. Once per second it starts a new unit of work
with its own correlation ID and logs a heartbeat inside a correlation ID logging scope.

```csharp
public class Worker : BackgroundService, IHostedService, IDisposable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BackgroundService](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice) ← 
[Worker](ONIONARCH.Presentation.Console.Worker.md)

#### Implements

[IHostedService](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostedservice), 
[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable)

#### Inherited Members

[BackgroundService.Dispose\(\)](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice.dispose), 
[BackgroundService.ExecuteAsync\(CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice.executeasync), 
[BackgroundService.StartAsync\(CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice.startasync), 
[BackgroundService.StopAsync\(CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice.stopasync), 
[BackgroundService.ExecuteTask](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.backgroundservice.executetask), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Presentation_Console_Worker__ctor_Microsoft_Extensions_Logging_ILogger_ONIONARCH_Presentation_Console_Worker__ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor_"></a> Worker\(ILogger<Worker\>, CorrelationIdAccessor\)

Sample background worker for the console host. Once per second it starts a new unit of work
with its own correlation ID and logs a heartbeat inside a correlation ID logging scope.

```csharp
public Worker(ILogger<Worker> logger, CorrelationIdAccessor correlationIdAccessor)
```

#### Parameters

`logger` [ILogger](https://learn.microsoft.com/dotnet/api/microsoft.extensions.logging.ilogger\-1)<[Worker](ONIONARCH.Presentation.Console.Worker.md)\>

The logger used for heartbeat entries.

`correlationIdAccessor` CorrelationIdAccessor

The ambient correlation ID store.

## Methods

### <a id="ONIONARCH_Presentation_Console_Worker_ExecuteAsync_System_Threading_CancellationToken_"></a> ExecuteAsync\(CancellationToken\)

Runs the worker loop until the host signals shutdown.

```csharp
protected override Task ExecuteAsync(CancellationToken stoppingToken)
```

#### Parameters

`stoppingToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

Signaled when the host is stopping.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the loop exits.

