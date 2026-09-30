# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkDeleteSampleEntityEFCoreRequest"></a> Class BulkDeleteSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to delete many sample entities with one set-based <code>DELETE</code> through the EF Core bulk
port ([IBulkCommandDbContext.DeleteWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_DeleteWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

```csharp
public sealed record BulkDeleteSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<BulkDeleteSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BulkDeleteSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkDeleteSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<BulkDeleteSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkDeleteSampleEntityEFCoreRequest__ctor_System_Collections_Generic_IReadOnlyCollection_System_Int32__"></a> BulkDeleteSampleEntityEFCoreRequest\(IReadOnlyCollection<int\>\)

Command to delete many sample entities with one set-based <code>DELETE</code> through the EF Core bulk
port ([IBulkCommandDbContext.DeleteWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_DeleteWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

```csharp
public BulkDeleteSampleEntityEFCoreRequest(IReadOnlyCollection<int> SampleIds)
```

#### Parameters

`SampleIds` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The keys of the entities to delete.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_BulkDeleteSampleEntityEFCoreRequest_SampleIds"></a> SampleIds

The keys of the entities to delete.

```csharp
public IReadOnlyCollection<int> SampleIds { get; init; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

