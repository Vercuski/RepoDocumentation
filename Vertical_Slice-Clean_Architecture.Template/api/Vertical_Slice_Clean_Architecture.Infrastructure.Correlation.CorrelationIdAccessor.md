# <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdAccessor"></a> Class CorrelationIdAccessor

Namespace: [Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Infrastructure.dll  

Gives access to the current operation's correlation ID. The value is held in an
[AsyncLocal](https://learn.microsoft.com/dotnet/api/system.threading.asynclocal-1), so it flows through the whole async call chain of a request (every
await, handler and data-access call) without being passed as a parameter.

```csharp
public sealed class CorrelationIdAccessor
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CorrelationIdAccessor](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Correlation.CorrelationIdAccessor.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
Registered as a singleton by <code>AddInfrastructureRegistration()</code>; inject it wherever the ID is
needed (for example to forward it on outgoing HTTP calls). That is safe because the backing
[AsyncLocal](https://learn.microsoft.com/dotnet/api/system.threading.asynclocal-1) is static and keeps a separate value per async flow, so concurrent
requests never see each other's IDs.
</p>
<p>
[CorrelationIdMiddleware](Vertical_Slice_Clean_Architecture.Infrastructure.Correlation.CorrelationIdMiddleware.md) sets the value at the start of every HTTP request.
</p>

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdAccessor_CorrelationId"></a> CorrelationId

Gets the correlation ID for the current async flow, or [Empty](https://learn.microsoft.com/dotnet/api/system.string.empty) outside a
request (for example during startup or in a background service).

```csharp
public string CorrelationId { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Infrastructure_Correlation_CorrelationIdAccessor_Set_System_String_"></a> Set\(string\)

Sets the correlation ID for the current async flow and every flow it subsequently starts.

```csharp
public void Set(string correlationId)
```

#### Parameters

`correlationId` [string](https://learn.microsoft.com/dotnet/api/system.string)

The correlation ID to make ambient.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

<code class="paramref">correlationId</code> is null, empty, or whitespace.

