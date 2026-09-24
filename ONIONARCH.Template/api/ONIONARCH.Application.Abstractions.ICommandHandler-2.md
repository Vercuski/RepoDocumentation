# <a id="ONIONARCH_Application_Abstractions_ICommandHandler_2"></a> Interface ICommandHandler<TCommand, TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Handles a state-changing [ICommandRequest<TResponse\>](ONIONARCH.Application.Abstractions.ICommandRequest-1.md).

```csharp
public interface ICommandHandler<in TCommand, TResponse> : IRequestHandler<TCommand, TResponse> where TCommand : ICommandRequest<TResponse>
```

#### Type Parameters

`TCommand` 

The command type this handler processes.

`TResponse` 

The type of response the command produces.

#### Implements

[IRequestHandler<TCommand, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler\-2.md)

## Remarks

Adds no members to [IRequestHandler<TRequest, TResponse\>](ONIONARCH.Application.Abstractions.IRequestHandler-2.md); it is a semantic marker
that the architecture fitness tests use to require command handlers to be sealed and to take a
command-side persistence abstraction in their constructor.

