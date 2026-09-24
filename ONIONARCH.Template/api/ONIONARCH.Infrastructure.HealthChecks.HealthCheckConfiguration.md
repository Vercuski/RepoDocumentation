# <a id="ONIONARCH_Infrastructure_HealthChecks_HealthCheckConfiguration"></a> Class HealthCheckConfiguration

Namespace: [ONIONARCH.Infrastructure.HealthChecks](ONIONARCH.Infrastructure.HealthChecks.md)  
Assembly: ONIONARCH.Infrastructure.dll  

Formats health check results for the <code>/health</code> endpoint.

```csharp
public class HealthCheckConfiguration
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[HealthCheckConfiguration](ONIONARCH.Infrastructure.HealthChecks.HealthCheckConfiguration.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Infrastructure_HealthChecks_HealthCheckConfiguration__ctor"></a> HealthCheckConfiguration\(\)

Prevents instantiation; this type only exposes static members.

```csharp
protected HealthCheckConfiguration()
```

## Methods

### <a id="ONIONARCH_Infrastructure_HealthChecks_HealthCheckConfiguration_WriteResponse_Microsoft_AspNetCore_Http_HttpContext_Microsoft_Extensions_Diagnostics_HealthChecks_HealthReport_"></a> WriteResponse\(HttpContext, HealthReport\)

Writes <code class="paramref">healthReport</code> to the response as indented JSON containing the
overall status, the application version ([ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)), and, for each
registered check, its status, description, and data.

```csharp
public static Task WriteResponse(HttpContext context, HealthReport healthReport)
```

#### Parameters

`context` [HttpContext](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpcontext)

The HTTP context of the health check request.

`healthReport` [HealthReport](https://learn.microsoft.com/dotnet/api/microsoft.extensions.diagnostics.healthchecks.healthreport)

The aggregated health check results.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the response body has been written.

#### Examples

<pre><code class="lang-csharp">{
  "status": "Healthy",
  "version": "1.4.1-alpha.0.3",
  "informationalVersion": "1.4.1-alpha.0.3+2057147a6910abdd18c2360adb13dea4c2cb3df6",
  "results": {
    "SimpleHealthCheck": { "status": "Healthy", "description": "Value was 3", "data": { "Value": 3 } }
  }
}</code></pre>

