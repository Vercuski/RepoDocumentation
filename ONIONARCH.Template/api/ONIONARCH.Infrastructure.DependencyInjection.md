# <a id="ONIONARCH_Infrastructure_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Infrastructure](ONIONARCH.Infrastructure.md)  
Assembly: ONIONARCH.Infrastructure.dll  

Composition-root extensions that register and wire up the Infrastructure layer's
cross-cutting services (health checks, logging, correlation IDs, problem details).

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Infrastructure.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Infrastructure_DependencyInjection_AddInfrastructureApplicationRegistration_Microsoft_AspNetCore_Builder_WebApplication_"></a> AddInfrastructureApplicationRegistration\(WebApplication\)

Maps the <code>/health</code> endpoint, formatting the report with
[HealthCheckConfiguration.WriteResponse](ONIONARCH.Infrastructure.HealthChecks.HealthCheckConfiguration.md#ONIONARCH_Infrastructure_HealthChecks_HealthCheckConfiguration_WriteResponse_Microsoft_AspNetCore_Http_HttpContext_Microsoft_Extensions_Diagnostics_HealthChecks_HealthReport_).

```csharp
public static WebApplication? AddInfrastructureApplicationRegistration(this WebApplication app)
```

#### Parameters

`app` [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)

The web application to configure.

#### Returns

 [WebApplication](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.builder.webapplication)?

The same <code class="paramref">app</code>, for chaining.

### <a id="ONIONARCH_Infrastructure_DependencyInjection_AddInfrastructureRegistration_Microsoft_Extensions_Hosting_IHostApplicationBuilder_"></a> AddInfrastructureRegistration\(IHostApplicationBuilder\)

Registers the Infrastructure layer's services: health checks, logging providers,
the singleton [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md), the singleton [ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)
(plus a hosted service that logs it at startup), and ProblemDetails support.

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

<code>AddProblemDetails()</code> is required when a host pairs <code>AddExceptionHandler&lt;T&gt;()</code>
with the parameterless <code>UseExceptionHandler()</code>; without it the host throws at startup.

### <a id="ONIONARCH_Infrastructure_DependencyInjection_UseCorrelationIdMiddleware_Microsoft_AspNetCore_Builder_WebApplication_"></a> UseCorrelationIdMiddleware\(WebApplication\)

Adds [CorrelationIdMiddleware](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md) to the request pipeline.

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

Call this before <code>UseExceptionHandler()</code> so the correlation ID is already set when
the global exception handler builds its response.

