# <a id="ONIONARCH_Infrastructure_Correlation"></a> Namespace ONIONARCH.Infrastructure.Correlation

### Classes

 [CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md)

Ambient accessor for the current operation's correlation ID, backed by AsyncLocal so the
value flows implicitly through the entire async call chain of a single request — every
downstream await, request handler, and repository call sees it without it being passed
as a parameter anywhere.

 [CorrelationIdMiddleware](ONIONARCH.Infrastructure.Correlation.CorrelationIdMiddleware.md)

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

