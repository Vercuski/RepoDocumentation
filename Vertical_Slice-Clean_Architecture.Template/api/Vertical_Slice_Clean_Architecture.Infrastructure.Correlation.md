# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation"></a> Namespace Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation

### Classes

 [CorrelationIdAccessor](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md)

Gives access to the current operation's correlation ID. The value is held in an
[AsyncLocal](https://learn.microsoft.com/dotnet/api/system.threading.asynclocal-1), so it flows through the whole async call chain of a request (every
await, handler and data-access call) without being passed as a parameter.

 [CorrelationIdMiddleware](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md)

ASP.NET Core middleware that establishes a correlation ID for every HTTP request.

