# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpsertSampleEntityEFCoreRequest"></a> Class BulkUpsertSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to insert or update many sample entities by key in one bulk operation through the EF Core
bulk port.

```csharp
public sealed record BulkUpsertSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<BulkUpsertSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BulkUpsertSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkUpsertSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<BulkUpsertSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpsertSampleEntityEFCoreRequest__ctor_System_Collections_Generic_IReadOnlyCollection_ONIONARCH_Domain_Entities_SampleEntityDefinition__"></a> BulkUpsertSampleEntityEFCoreRequest\(IReadOnlyCollection<SampleEntityDefinition\>\)

Command to insert or update many sample entities by key in one bulk operation through the EF Core
bulk port.

```csharp
public BulkUpsertSampleEntityEFCoreRequest(IReadOnlyCollection<SampleEntityDefinition> SampleEntities)
```

#### Parameters

`SampleEntities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<SampleEntityDefinition\>

The entities to write. An entity whose key matches an existing row updates it; one with an unsaved
key (<code>0</code>) is inserted.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpsertSampleEntityEFCoreRequest_SampleEntities"></a> SampleEntities

The entities to write. An entity whose key matches an existing row updates it; one with an unsaved
key (<code>0</code>) is inserted.

```csharp
public IReadOnlyCollection<SampleEntityDefinition> SampleEntities { get; init; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<SampleEntityDefinition\>

