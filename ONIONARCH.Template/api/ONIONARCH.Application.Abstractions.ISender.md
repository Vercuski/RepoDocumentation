# <a id="ONIONARCH_Application_Abstractions_ISender"></a> Interface ISender

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Single dispatch chokepoint for the CQRS pipeline. Presentation depends only on this interface
and on request/response contract types — never on a concrete handler — which is the same
decoupling MediatR's IMediator previously provided.

```csharp
public interface ISender
```

## Methods

### <a id="ONIONARCH_Application_Abstractions_ISender_Send__1_ONIONARCH_Application_Abstractions_IAppRequest___0__System_Threading_CancellationToken_"></a> Send<TResponse\>\(IAppRequest<TResponse\>, CancellationToken\)

Dispatches <code class="paramref">request</code> through every registered
[IPipelineBehavior<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IPipelineBehavior-2.md) to its single
[IRequestHandler<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler-2.md).

```csharp
Task<TResponse> Send<TResponse>(IAppRequest<TResponse> request, CancellationToken cancellationToken = default)
```

#### Parameters

`request` [IAppRequest](ONIONARCH.Application.Abstractions.IAppRequest\-1.md)<TResponse\>

The query or command to dispatch.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>

The response produced by the request's handler.

#### Type Parameters

`TResponse` 

The response type declared by the request.

#### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

No handler is registered for the request's runtime type.

