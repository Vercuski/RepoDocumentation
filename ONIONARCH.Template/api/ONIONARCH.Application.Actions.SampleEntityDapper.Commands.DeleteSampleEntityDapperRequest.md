# <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_DeleteSampleEntityDapperRequest"></a> Class DeleteSampleEntityDapperRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityDapper.Commands](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to delete a sample entity by key through the Dapper persistence path.

```csharp
public sealed record DeleteSampleEntityDapperRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<DeleteSampleEntityDapperRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DeleteSampleEntityDapperRequest](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.DeleteSampleEntityDapperRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<DeleteSampleEntityDapperRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_DeleteSampleEntityDapperRequest__ctor_System_Int32_"></a> DeleteSampleEntityDapperRequest\(int\)

Command to delete a sample entity by key through the Dapper persistence path.

```csharp
public DeleteSampleEntityDapperRequest(int SampleId)
```

#### Parameters

`SampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the entity to delete.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_DeleteSampleEntityDapperRequest_SampleId"></a> SampleId

The key of the entity to delete.

```csharp
public int SampleId { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

