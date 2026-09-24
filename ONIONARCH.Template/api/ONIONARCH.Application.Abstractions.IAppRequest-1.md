# <a id="ONIONARCH_Application_Abstractions_IAppRequest_1"></a> Interface IAppRequest<TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Base marker for anything dispatchable through [ISender](ONIONARCH.Application.Abstractions.ISender.md). Deliberately carries no
members — it exists purely so [ISender.Send<TResponse\>](ONIONARCH.Application.Abstractions.ISender.md#ONIONARCH_Application_Abstractions_ISender_Send__1_ONIONARCH_Application_Abstractions_IAppRequest___0__System_Threading_CancellationToken_) and
[IPipelineBehavior<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IPipelineBehavior-2.md) have a single covariant type to close
their generics over, regardless of whether the concrete request is a query or a command.

```csharp
public interface IAppRequest<out TResponse>
```

#### Type Parameters

`TResponse` 

The type of response the request's handler produces.

## Remarks

Request types should implement [IQueryRequest<TResponse\>](ONIONARCH.Application.Abstractions.IQueryRequest-1.md) or
[ICommandRequest<TResponse\>](ONIONARCH.Application.Abstractions.ICommandRequest-1.md) rather than this interface directly.

