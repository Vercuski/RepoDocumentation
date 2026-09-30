# <a id="ONIONARCH_Application_Contracts_Dtos_BulkUpdateSampleRequestDto"></a> Class BulkUpdateSampleRequestDto

Namespace: [ONIONARCH.Application.Contracts.Dtos](ONIONARCH.Application.Contracts.Dtos.md)  
Assembly: ONIONARCH.Application.dll  

Inbound payload for a set-based update of many sample entities.

```csharp
public sealed record BulkUpdateSampleRequestDto : IEquatable<BulkUpdateSampleRequestDto>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[BulkUpdateSampleRequestDto](ONIONARCH.Application.Contracts.Dtos.BulkUpdateSampleRequestDto.md)

#### Implements

[IEquatable<BulkUpdateSampleRequestDto\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Contracts_Dtos_BulkUpdateSampleRequestDto__ctor_System_Collections_Generic_IReadOnlyList_System_Int32__System_Boolean_System_Int32_"></a> BulkUpdateSampleRequestDto\(IReadOnlyList<int\>, bool, int\)

Inbound payload for a set-based update of many sample entities.

```csharp
public BulkUpdateSampleRequestDto(IReadOnlyList<int> DtoSampleIds, bool DtoSampleBoolean, int DtoSampleIntIncrement)
```

#### Parameters

`DtoSampleIds` [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The keys of the entities to update.

`DtoSampleBoolean` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

The value to assign to [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

`DtoSampleIntIncrement` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The amount to add to each entity's current [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

## Properties

### <a id="ONIONARCH_Application_Contracts_Dtos_BulkUpdateSampleRequestDto_DtoSampleBoolean"></a> DtoSampleBoolean

The value to assign to [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

```csharp
public bool DtoSampleBoolean { get; init; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Contracts_Dtos_BulkUpdateSampleRequestDto_DtoSampleIds"></a> DtoSampleIds

The keys of the entities to update.

```csharp
public IReadOnlyList<int> DtoSampleIds { get; init; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

### <a id="ONIONARCH_Application_Contracts_Dtos_BulkUpdateSampleRequestDto_DtoSampleIntIncrement"></a> DtoSampleIntIncrement

The amount to add to each entity's current [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

```csharp
public int DtoSampleIntIncrement { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

