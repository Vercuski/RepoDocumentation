# <a id="ONIONARCH_Application_Abstractions_IQueryHandler_2"></a> Interface IQueryHandler<TQuery, TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Handles a read-only [IQueryRequest<TResponse\>](ONIONARCH.Application.Abstractions.IQueryRequest-1.md).

```csharp
public interface IQueryHandler<in TQuery, TResponse> : IRequestHandler<TQuery, TResponse> where TQuery : IQueryRequest<TResponse>
```

#### Type Parameters

`TQuery` 

The query type this handler processes.

`TResponse` 

The type of response the query produces.

#### Implements

[IRequestHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler\-2.md)

## Remarks

Adds no members to [IRequestHandler<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler-2.md); it is a semantic marker
that the architecture fitness tests use to require query handlers to be sealed and to take a
query-side persistence abstraction in their constructor.

