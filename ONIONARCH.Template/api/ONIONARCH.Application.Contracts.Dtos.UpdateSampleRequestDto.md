# <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto"></a> Class UpdateSampleRequestDto

Namespace: [ONIONARCH.Application.Contracts.Dtos](ONIONARCH.Application.Contracts.Dtos.md)  
Assembly: ONIONARCH.Application.dll  

Inbound payload for updating an existing sample entity.

```csharp
public sealed record UpdateSampleRequestDto : IDomainMapper<SampleEntityDefinition>, IEquatable<UpdateSampleRequestDto>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[UpdateSampleRequestDto](ONIONARCH.Application.Contracts.Dtos.UpdateSampleRequestDto.md)

#### Implements

[IDomainMapper<SampleEntityDefinition\>](ONIONARCH.Application.Abstractions.IDomainMapper\-1.md), 
[IEquatable<UpdateSampleRequestDto\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto__ctor_System_Int32_System_String_System_Boolean_System_Int32_System_Decimal_"></a> UpdateSampleRequestDto\(int, string?, bool, int, decimal\)

Inbound payload for updating an existing sample entity.

```csharp
public UpdateSampleRequestDto(int DtoSampleId, string? DtoSampleString, bool DtoSampleBoolean, int DtoSampleInt, decimal DtoSampleDecimal)
```

#### Parameters

`DtoSampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the entity to update.

`DtoSampleString` [string](https://learn.microsoft.com/dotnet/api/system.string)?

The new value for [SampleEntityDefinition.SampleString](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleString).

`DtoSampleBoolean` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

The new value for [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

`DtoSampleInt` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The new value for [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

`DtoSampleDecimal` [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

The new value for [SampleEntityDefinition.SampleDecimal](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleDecimal).

## Properties

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_DtoSampleBoolean"></a> DtoSampleBoolean

The new value for [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

```csharp
public bool DtoSampleBoolean { get; init; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_DtoSampleDecimal"></a> DtoSampleDecimal

The new value for [SampleEntityDefinition.SampleDecimal](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleDecimal).

```csharp
public decimal DtoSampleDecimal { get; init; }
```

#### Property Value

 [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_DtoSampleId"></a> DtoSampleId

The key of the entity to update.

```csharp
public int DtoSampleId { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_DtoSampleInt"></a> DtoSampleInt

The new value for [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

```csharp
public int DtoSampleInt { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_DtoSampleString"></a> DtoSampleString

The new value for [SampleEntityDefinition.SampleString](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleString).

```csharp
public string? DtoSampleString { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

## Methods

### <a id="ONIONARCH_Application_Contracts_Dtos_UpdateSampleRequestDto_MapToDomain"></a> MapToDomain\(\)

Creates a [SampleEntityDefinition](ONIONARCH.Domain.Entities.SampleEntityDefinition.md) carrying this payload's key and values.

```csharp
public SampleEntityDefinition MapToDomain()
```

#### Returns

 SampleEntityDefinition

A new, detached sample entity ready to be passed to an update command.

