# <a id="ONIONARCH_Application_Abstractions_IPipelineBehavior_2"></a> Interface IPipelineBehavior<TRequest, TResponse\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Cross-cutting wrapper around a request/handler pair, resolved and chained by [ONIONARCH.Application.Sender](ONIONARCH.Application.md)
for every dispatched request regardless of its concrete type. Mirrors MediatR's
IPipelineBehavior&lt;TRequest,TResponse&gt; shape closely enough that behaviors written for it (see
[LoggingBehavior<TRequest, TResponse\>](ONIONARCH.Application.Behaviors.LoggingBehavior-2.md)) only need their
<code>next</code> delegate signature updated.

```csharp
public interface IPipelineBehavior<TRequest, TResponse> where TRequest : IAppRequest<TResponse>
```

#### Type Parameters

`TRequest` 

The request type being dispatched.

`TResponse` 

The response type produced by the request's handler.

## Remarks

Register open-generic implementations against <code>IPipelineBehavior&lt;,&gt;</code>; behaviors run in
registration order, with the first-registered behavior outermost.

## Methods

### <a id="ONIONARCH_Application_Abstractions_IPipelineBehavior_2_Handle__0_System_Func_System_Threading_Tasks_Task__1___System_Threading_CancellationToken_"></a> Handle\(TRequest, Func<Task<TResponse\>\>, CancellationToken\)

Executes this behavior's logic around the rest of the pipeline.

```csharp
Task<TResponse> Handle(TRequest request, Func<Task<TResponse>> next, CancellationToken cancellationToken)
```

#### Parameters

`request` TRequest

The request being dispatched.

`next` [Func](https://learn.microsoft.com/dotnet/api/system.func\-1)<[Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>\>

Invokes the next behavior in the chain, or the request handler if this is the innermost
behavior. A behavior may short-circuit by not calling it.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TResponse\>

The response produced by <code class="paramref">next</code>, or a substitute response.

