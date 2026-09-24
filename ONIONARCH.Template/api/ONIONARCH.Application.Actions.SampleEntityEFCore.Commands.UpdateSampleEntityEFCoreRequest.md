# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_UpdateSampleEntityEFCoreRequest"></a> Class UpdateSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to update an existing sample entity through the EF Core persistence path.

```csharp
public sealed record UpdateSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<UpdateSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.UpdateSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<UpdateSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_UpdateSampleEntityEFCoreRequest__ctor_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> UpdateSampleEntityEFCoreRequest\(SampleEntityDefinition\)

Command to update an existing sample entity through the EF Core persistence path.

```csharp
public UpdateSampleEntityEFCoreRequest(SampleEntityDefinition SampleEntity)
```

#### Parameters

`SampleEntity` SampleEntityDefinition

The entity carrying the key and new values.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_UpdateSampleEntityEFCoreRequest_SampleEntity"></a> SampleEntity

The entity carrying the key and new values.

```csharp
public SampleEntityDefinition SampleEntity { get; init; }
```

#### Property Value

 SampleEntityDefinition

