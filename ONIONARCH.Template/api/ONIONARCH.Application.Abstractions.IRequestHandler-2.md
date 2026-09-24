# <a id="ONIONARCH_Application_Abstractions_IRequestHandler_2"></a> Interface IRequestHandler<TRequest, TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Base handler contract. [ONIONARCH.Application.Sender](ONIONARCH.Application.md) always resolves the closed generic
<code>IRequestHandler&lt;TRequest, TResponse&gt;</code> for the request's runtime type — it never needs
to know whether the concrete request is a query or a command. [IQueryHandler<TQuery, TResponse\>](ONIONARCH.Application.Abstractions.IQueryHandler-2.md)
and [ICommandHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.ICommandHandler-2.md) exist purely as semantic/namespace markers for
handler authors and the architecture fitness tests; interface inheritance means a type implementing
either of them is still discoverable here via reflection's <code>Type.GetInterfaces()</code>.

```csharp
public interface IRequestHandler<in TRequest, TResponse> where TRequest : IAppRequest<TResponse>
```

#### Type Parameters

`TRequest` 

The request type this handler processes.

`TResponse` 

The type of response the handler produces.

## Methods

### <a id="ONIONARCH_Application_Abstractions_IRequestHandler_2_Handle__0_System_Threading_CancellationToken_"></a> Handle\(TRequest, CancellationToken\)

Handles <code class="paramref">request</code> and produces its response.

```csharp
Task<TResponse> Handle(TRequest request, CancellationToken cancellationToken)
```

#### Parameters

`request` TRequest

The request to handle.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>

The response for the request.

