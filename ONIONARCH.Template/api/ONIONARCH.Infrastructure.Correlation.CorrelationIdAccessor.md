# <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor"></a> Class CorrelationIdAccessor

Namespace: [ONIONARCH.Infrastructure.Correlation](ONIONARCH.Infrastructure.Correlation.md)  
Assembly: ONIONARCH.Infrastructure.dll  

Ambient accessor for the current operation's correlation ID, backed by AsyncLocal so the
value flows implicitly through the entire async call chain of a single request — every
downstream await, request handler, and repository call sees it without it being passed
as a parameter anywhere.

```csharp
public sealed class CorrelationIdAccessor
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CorrelationIdAccessor](ONIONARCH.Infrastructure.Correlation.CorrelationIdAccessor.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Registered as a singleton. That is safe because the backing [AsyncLocal](https://learn.microsoft.com/dotnet/api/system.threading.asynclocal-1) is
static and isolates its value per async execution flow, so concurrent requests never see
each other's IDs.

## Properties

### <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor_CorrelationId"></a> CorrelationId

Gets the correlation ID for the current async flow, or [Empty](https://learn.microsoft.com/dotnet/api/system.string.empty) if none has been set.

```csharp
public string CorrelationId { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="ONIONARCH_Infrastructure_Correlation_CorrelationIdAccessor_Set_System_String_"></a> Set\(string\)

Sets the correlation ID for the current async flow and every flow it subsequently spawns.

```csharp
public void Set(string correlationId)
```

#### Parameters

`correlationId` [string](https://learn.microsoft.com/dotnet/api/system.string)

The correlation ID to make ambient.

