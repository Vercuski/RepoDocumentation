# <a id="ONIONARCH_Infrastructure_HealthChecks"></a> Namespace ONIONARCH.Infrastructure.HealthChecks

### Classes

 [HealthCheckConfiguration](ONIONARCH.Infrastructure.HealthChecks.HealthCheckConfiguration.md)

Formats health check results for the <code>/health</code> endpoint.

 [SimpleHealthCheck](ONIONARCH.Infrastructure.HealthChecks.SimpleHealthCheck.md)

Demonstration health check that randomly reports Unhealthy, Degraded, or Healthy so the
<code>/health</code> endpoint's output for each status can be observed. Replace the code between the
Start/End markers with a real probe (database, downstream service, etc.).

