# <a id="ONIONARCH_Application_Abstractions_ICommandRequest_1"></a> Interface ICommandRequest<TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Marker for a CQRS command — a request that changes system state. Handled by an
[ICommandHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.ICommandHandler-2.md).

```csharp
public interface ICommandRequest<out TResponse> : IAppRequest<TResponse>
```

#### Type Parameters

`TResponse` 

The type of response the command produces.

#### Implements

[IAppRequest<TResponse\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md)

