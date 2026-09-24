# <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_CreateSampleEntityDapperRequest"></a> Class CreateSampleEntityDapperRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityDapper.Commands](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to insert a new sample entity through the Dapper persistence path.

```csharp
public sealed record CreateSampleEntityDapperRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<CreateSampleEntityDapperRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreateSampleEntityDapperRequest](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.CreateSampleEntityDapperRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<CreateSampleEntityDapperRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_CreateSampleEntityDapperRequest__ctor_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> CreateSampleEntityDapperRequest\(SampleEntityDefinition\)

Command to insert a new sample entity through the Dapper persistence path.

```csharp
public CreateSampleEntityDapperRequest(SampleEntityDefinition SampleEntity)
```

#### Parameters

`SampleEntity` SampleEntityDefinition

The entity to insert.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_CreateSampleEntityDapperRequest_SampleEntity"></a> SampleEntity

The entity to insert.

```csharp
public SampleEntityDefinition SampleEntity { get; init; }
```

#### Property Value

 SampleEntityDefinition

