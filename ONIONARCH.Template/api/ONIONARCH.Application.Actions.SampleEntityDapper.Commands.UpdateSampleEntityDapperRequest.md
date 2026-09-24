# <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_UpdateSampleEntityDapperRequest"></a> Class UpdateSampleEntityDapperRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityDapper.Commands](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to update an existing sample entity through the Dapper persistence path.

```csharp
public sealed record UpdateSampleEntityDapperRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<UpdateSampleEntityDapperRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdateSampleEntityDapperRequest](ONIONARCH.Application.Actions.SampleEntityDapper.Commands.UpdateSampleEntityDapperRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<UpdateSampleEntityDapperRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_UpdateSampleEntityDapperRequest__ctor_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> UpdateSampleEntityDapperRequest\(SampleEntityDefinition\)

Command to update an existing sample entity through the Dapper persistence path.

```csharp
public UpdateSampleEntityDapperRequest(SampleEntityDefinition SampleEntity)
```

#### Parameters

`SampleEntity` SampleEntityDefinition

The entity carrying the key and new values.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Commands_UpdateSampleEntityDapperRequest_SampleEntity"></a> SampleEntity

The entity carrying the key and new values.

```csharp
public SampleEntityDefinition SampleEntity { get; init; }
```

#### Property Value

 SampleEntityDefinition

