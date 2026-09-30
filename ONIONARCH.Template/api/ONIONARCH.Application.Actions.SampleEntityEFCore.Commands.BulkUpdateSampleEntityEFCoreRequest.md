# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpdateSampleEntityEFCoreRequest"></a> Class BulkUpdateSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to update many sample entities with one set-based <code>UPDATE</code> through the EF Core bulk
port ([IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

```csharp
public sealed record BulkUpdateSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<BulkUpdateSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BulkUpdateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkUpdateSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<BulkUpdateSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpdateSampleEntityEFCoreRequest__ctor_System_Collections_Generic_IReadOnlyCollection_System_Int32__System_Boolean_System_Int32_"></a> BulkUpdateSampleEntityEFCoreRequest\(IReadOnlyCollection<int\>, bool, int\)

Command to update many sample entities with one set-based <code>UPDATE</code> through the EF Core bulk
port ([IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

```csharp
public BulkUpdateSampleEntityEFCoreRequest(IReadOnlyCollection<int> SampleIds, bool SampleBoolean, int SampleIntIncrement)
```

#### Parameters

`SampleIds` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The keys of the entities to update.

`SampleBoolean` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

The value to assign to [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

`SampleIntIncrement` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The amount to add to each entity's current [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpdateSampleEntityEFCoreRequest_SampleBoolean"></a> SampleBoolean

The value to assign to [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

```csharp
public bool SampleBoolean { get; init; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpdateSampleEntityEFCoreRequest_SampleIds"></a> SampleIds

The keys of the entities to update.

```csharp
public IReadOnlyCollection<int> SampleIds { get; init; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkUpdateSampleEntityEFCoreRequest_SampleIntIncrement"></a> SampleIntIncrement

The amount to add to each entity's current [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

```csharp
public int SampleIntIncrement { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

