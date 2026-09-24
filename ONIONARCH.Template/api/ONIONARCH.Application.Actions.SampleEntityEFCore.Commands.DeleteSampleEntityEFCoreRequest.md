# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_DeleteSampleEntityEFCoreRequest"></a> Class DeleteSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to delete a sample entity through the EF Core persistence path.

```csharp
public sealed record DeleteSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<DeleteSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DeleteSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.DeleteSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<DeleteSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_DeleteSampleEntityEFCoreRequest__ctor_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> DeleteSampleEntityEFCoreRequest\(SampleEntityDefinition\)

Command to delete a sample entity through the EF Core persistence path.

```csharp
public DeleteSampleEntityEFCoreRequest(SampleEntityDefinition Entity)
```

#### Parameters

`Entity` SampleEntityDefinition

The entity to delete. The caller is expected to have loaded it first (the API does so via
<code>GetSingleSampleEntityEFCoreRequest</code>) so a missing entity is reported as not-found.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_DeleteSampleEntityEFCoreRequest_Entity"></a> Entity

The entity to delete. The caller is expected to have loaded it first (the API does so via
<code>GetSingleSampleEntityEFCoreRequest</code>) so a missing entity is reported as not-found.

```csharp
public SampleEntityDefinition Entity { get; init; }
```

#### Property Value

 SampleEntityDefinition

