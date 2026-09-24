# <a id="ONIONARCH_Infrastructure_HealthChecks_SimpleHealthCheck"></a> Class SimpleHealthCheck

Namespace: [ONIONARCH.Infrastructure.HealthChecks](ONIONARCH.Infrastructure.HealthChecks.md)  
Assembly: ONIONARCH.Infrastructure.dll  

Demonstration health check that randomly reports Unhealthy, Degraded, or Healthy so the
<code>/health</code> endpoint's output for each status can be observed. Replace the code between the
Start/End markers with a real probe (database, downstream service, etc.).

```csharp
public class SimpleHealthCheck : IHealthCheck
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SimpleHealthCheck](ONIONARCH.Infrastructure.HealthChecks.SimpleHealthCheck.md)

#### Implements

[IHealthCheck](https://learn.microsoft.com/dotnet/api/microsoft.extensions.diagnostics.healthchecks.ihealthcheck)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Discovered and registered automatically by the Infrastructure health check assembly scan.

## Methods

### <a id="ONIONARCH_Infrastructure_HealthChecks_SimpleHealthCheck_CheckHealthAsync_Microsoft_Extensions_Diagnostics_HealthChecks_HealthCheckContext_System_Threading_CancellationToken_"></a> CheckHealthAsync\(HealthCheckContext, CancellationToken\)

Runs the health check.

```csharp
public Task<HealthCheckResult> CheckHealthAsync(HealthCheckContext context, CancellationToken cancellationToken = default)
```

#### Parameters

`context` [HealthCheckContext](https://learn.microsoft.com/dotnet/api/microsoft.extensions.diagnostics.healthchecks.healthcheckcontext)

Context for the health check registration being evaluated.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the check.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[HealthCheckResult](https://learn.microsoft.com/dotnet/api/microsoft.extensions.diagnostics.healthchecks.healthcheckresult)\>

A result whose status is chosen at random, with the random value included in its data.

