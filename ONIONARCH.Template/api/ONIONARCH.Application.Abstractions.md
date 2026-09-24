# <a id="ONIONARCH_Application_Abstractions"></a> Namespace ONIONARCH.Application.Abstractions

### Namespaces

 [ONIONARCH.Application.Abstractions.ConnectionFactory](ONIONARCH.Application.Abstractions.ConnectionFactory.md)

 [ONIONARCH.Application.Abstractions.Context](ONIONARCH.Application.Abstractions.Context.md)

 [ONIONARCH.Application.Abstractions.Repositories](ONIONARCH.Application.Abstractions.Repositories.md)

### Structs

 [Result<T\>](ONIONARCH.Application.Abstractions.Result\-1.md)

Outcome of a request handler: either a successful value or an expected business-flow failure.

### Interfaces

 [IAppRequest<TResponse\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md)

Base marker for anything dispatchable through [ISender](ONIONARCH.Application.Abstractions.ISender.md). Deliberately carries no
members — it exists purely so [ISender.Send<TResponse\>](ONIONARCH.Application.Abstractions.ISender.md#ONIONARCH_Application_Abstractions_ISender_Send__1_ONIONARCH_Application_Abstractions_IAppRequest___0__System_Threading_CancellationToken_) and
[IPipelineBehavior<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IPipelineBehavior-2.md) have a single covariant type to close
their generics over, regardless of whether the concrete request is a query or a command.

 [ICommandHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.ICommandHandler\-2.md)

Handles a state-changing [ICommandRequest<TResponse\>](ONIONARCH.Application.Abstractions.ICommandRequest-1.md).

 [ICommandRequest<TResponse\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md)

Marker for a CQRS command — a request that changes system state. Handled by an
[ICommandHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.ICommandHandler-2.md).

 [IDomainMapper<TEntity\>](ONIONARCH.Application.Abstractions.IDomainMapper\-1.md)

Implemented by inbound DTOs that know how to convert themselves into a domain entity.

 [IPipelineBehavior<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IPipelineBehavior\-2.md)

Cross-cutting wrapper around a request/handler pair, resolved and chained by [ONIONARCH.Application.Sender](ONIONARCH.Application.md)
for every dispatched request regardless of its concrete type. Mirrors MediatR's
IPipelineBehavior&lt;TRequest,TResponse&gt; shape closely enough that behaviors written for it (see
[LoggingBehavior<TRequest, TResponse\>](ONIONARCH.Application.Behaviors.LoggingBehavior-2.md)) only need their
<code>next</code> delegate signature updated.

 [IQueryHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IQueryHandler\-2.md)

Handles a read-only [IQueryRequest<TResponse\>](ONIONARCH.Application.Abstractions.IQueryRequest-1.md).

 [IQueryRequest<TResponse\>](ONIONARCH.Application.Abstractions.IQueryRequest\-1.md)

Marker for a CQRS query — a request that reads data without changing system state. Handled by an
[IQueryHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IQueryHandler-2.md).

 [IRequestHandler<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler\-2.md)

Base handler contract. [ONIONARCH.Application.Sender](ONIONARCH.Application.md) always resolves the closed generic
<code>IRequestHandler&lt;TRequest, TResponse&gt;</code> for the request's runtime type — it never needs
to know whether the concrete request is a query or a command. [IQueryHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IQueryHandler-2.md)
and [ICommandHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.ICommandHandler-2.md) exist purely as semantic/namespace markers for
handler authors and the architecture fitness tests; interface inheritance means a type implementing
either of them is still discoverable here via reflection's <code>Type.GetInterfaces()</code>.

 [ISender](ONIONARCH.Application.Abstractions.ISender.md)

Single dispatch chokepoint for the CQRS pipeline. Presentation depends only on this interface
and on request/response contract types — never on a concrete handler — which is the same
decoupling MediatR's IMediator previously provided.

 [IUnitOfWork](ONIONARCH.Application.Abstractions.IUnitOfWork.md)

Unit-of-work port over the command database. Lets Application code commit staged changes
asynchronously and group multiple operations in an explicit transaction without depending
on EF Core.

 [IUnitOfWorkTransaction](ONIONARCH.Application.Abstractions.IUnitOfWorkTransaction.md)

An explicit database transaction started by [IUnitOfWork.BeginTransactionAsync](ONIONARCH.Application.Abstractions.IUnitOfWork.md#ONIONARCH_Application_Abstractions_IUnitOfWork_BeginTransactionAsync_System_Threading_CancellationToken_).

### Enums

 [ResultErrorType](ONIONARCH.Application.Abstractions.ResultErrorType.md)

Categorizes an expected business-flow failure carried by a [Result<T\>](ONIONARCH.Application.Abstractions.Result-1.md).
Presentation maps each category to an HTTP status code.

