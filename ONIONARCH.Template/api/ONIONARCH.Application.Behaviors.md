# <a id="ONIONARCH_Application_Behaviors"></a> Namespace ONIONARCH.Application.Behaviors

### Classes

 [LoggingBehavior<TRequest, TResponse\>](ONIONARCH.Application.Behaviors.LoggingBehavior\-2.md)

Logs entry, successful completion, and failure of every command/query. Combined with
the ambient correlation-ID logging scope pushed by CorrelationIdMiddleware (Infrastructure),
this reconstructs the full "path" of a request through the CQRS pipeline without any handler
needing to know a correlation ID exists.

