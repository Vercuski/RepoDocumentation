# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_DependencyInjection"></a> Class DependencyInjection

Namespace: [Vertical\_Slice\_Clean\_Architecture.Infrastructure](Vertical\_Slice\_Clean\_Architecture.Infrastructure.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Infrastructure.dll  

Composition-root extensions that register and wire up the Infrastructure layer's
cross-cutting services (health checks, logging, correlation IDs, problem details).

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](Vertical\_Slice\_Clean\_Architecture.Infrastructure.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_DependencyInjection_AddInfrastructureApplicationRegistration_Microsoft_AspNetCore_Builder_WebApplication_"></a> AddInfrastructureApplicationRegistration\(WebApplication\)

Maps the health endpoints, both formatted with [HealthCheckConfiguration.WriteResponse](Vertical_Slice_Clean_Architecture.Infrastructure.HealthChecks.HealthCheckConfiguration.md#Vertical_Slice_Clean_Architecture_Infrastructure_HealthChecks_HealthCheckConfiguration_WriteResponse_Microsoft_AspNetCore_Http_HttpContext_Microsoft_Extensions_Diagnostics_HealthChecks_HealthReport_):

<ul><li>
    <code>/health/live</code> runs no checks, so it answers <code>200</code> whenever the process can serve
    requests. Use it for liveness probes: a failing dependency must not get the container restarted.
  </li><li>
    <code>/health</code> runs every registered check (including the database check) and answers
    <code>200</code> when healthy or degraded and <code>503</code> when unhealthy. Use it for readiness
    probes and monitoring.
  </li></ul>

```csharp
public static WebApplication AddInfrastructureApplicationRegistration(this WebApplication app)
```

#### Parameters

`app` [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)

The web application to configure.

#### Returns

 [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)

The same <code class="paramref">app</code>, for chaining.

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_DependencyInjection_AddInfrastructureRegistration_Microsoft_Extensions_Hosting_IHostApplicationBuilder_"></a> AddInfrastructureRegistration\(IHostApplicationBuilder\)

Registers the Infrastructure layer's services: health checks, logging providers,
the singleton [CorrelationIdAccessor](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md), the singleton [ApplicationVersion](Vertical_Slice_Clean_Architecture.Infrastructure.Versioning.ApplicationVersion.md)
(plus a hosted service that logs it at startup), ProblemDetails support, and persistence
(see <code>Persistence/PersistenceRegistration.cs</code>).

```csharp
public static IHostApplicationBuilder AddInfrastructureRegistration(this IHostApplicationBuilder builder)
```

#### Parameters

`builder` [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The host builder to register services with.

#### Returns

 [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The same <code class="paramref">builder</code>, for chaining.

#### Remarks

ProblemDetails support is what lets the parameterless <code>UseExceptionHandler()</code> and
<code>UseStatusCodePages()</code> write RFC 9457 bodies. Every body written through it carries a
<code>correlationId</code> member.

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_DependencyInjection_UseCorrelationIdMiddleware_Microsoft_AspNetCore_Builder_WebApplication_"></a> UseCorrelationIdMiddleware\(WebApplication\)

Adds [CorrelationIdMiddleware](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md) to the request pipeline.

```csharp
public static WebApplication UseCorrelationIdMiddleware(this WebApplication app)
```

#### Parameters

`app` [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)

The web application to configure.

#### Returns

 [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)

The same <code class="paramref">app</code>, for chaining.

#### Remarks

Call this first in the pipeline, before <code>UseExceptionHandler()</code>, so the correlation ID
is already set when an error response is written and when its log entries are created.

