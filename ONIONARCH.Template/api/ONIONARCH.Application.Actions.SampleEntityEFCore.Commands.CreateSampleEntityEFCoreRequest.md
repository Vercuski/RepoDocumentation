# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_CreateSampleEntityEFCoreRequest"></a> Class CreateSampleEntityEFCoreRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityEFCore.Commands](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.md)  
Assembly: ONIONARCH.Application.dll  

Command to insert a new sample entity through the EF Core persistence path.

```csharp
public sealed record CreateSampleEntityEFCoreRequest : ICommandRequest<Result<int>>, IAppRequest<Result<int>>, IEquatable<CreateSampleEntityEFCoreRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.CreateSampleEntityEFCoreRequest.md)

#### Implements

[ICommandRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.ICommandRequest\-1.md), 
[IAppRequest<Result<int\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<CreateSampleEntityEFCoreRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_CreateSampleEntityEFCoreRequest__ctor_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> CreateSampleEntityEFCoreRequest\(SampleEntityDefinition\)

Command to insert a new sample entity through the EF Core persistence path.

```csharp
public CreateSampleEntityEFCoreRequest(SampleEntityDefinition SampleEntity)
```

#### Parameters

`SampleEntity` SampleEntityDefinition

The entity to insert.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands_CreateSampleEntityEFCoreRequest_SampleEntity"></a> SampleEntity

The entity to insert.

```csharp
public SampleEntityDefinition SampleEntity { get; init; }
```

#### Property Value

 SampleEntityDefinition

