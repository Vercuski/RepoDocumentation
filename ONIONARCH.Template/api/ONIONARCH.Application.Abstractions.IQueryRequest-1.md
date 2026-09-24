# <a id="ONIONARCH_Application_Abstractions_IQueryRequest_1"></a> Interface IQueryRequest<TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Marker for a CQRS query — a request that reads data without changing system state. Handled by an
[IQueryHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IQueryHandler-2.md).

```csharp
public interface IQueryRequest<out TResponse> : IAppRequest<TResponse>
```

#### Type Parameters

`TResponse` 

The type of response the query produces.

#### Implements

[IAppRequest<TResponse\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md)

