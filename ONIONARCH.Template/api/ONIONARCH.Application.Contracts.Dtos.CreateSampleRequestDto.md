# <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto"></a> Class CreateSampleRequestDto

Namespace: [ONIONARCH.Application.Contracts.Dtos](ONIONARCH.Application.Contracts.Dtos.md)  
Assembly: ONIONARCH.Application.dll  

Inbound payload for creating a sample entity.

```csharp
public sealed record CreateSampleRequestDto : IDomainMapper<SampleEntityDefinition>, IEquatable<CreateSampleRequestDto>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[CreateSampleRequestDto](ONIONARCH.Application.Contracts.Dtos.CreateSampleRequestDto.md)

#### Implements

[IDomainMapper<SampleEntityDefinition\>](ONIONARCH.Application.Abstractions.IDomainMapper\-1.md), 
[IEquatable<CreateSampleRequestDto\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto__ctor_System_String_System_Boolean_System_Int32_System_Decimal_"></a> CreateSampleRequestDto\(string?, bool, int, decimal\)

Inbound payload for creating a sample entity.

```csharp
public CreateSampleRequestDto(string? DtoSampleString, bool DtoSampleBoolean, int DtoSampleInt, decimal DtoSampleDecimal)
```

#### Parameters

`DtoSampleString` [string](https://learn.microsoft.com/dotnet/api/system.string)?

The value for [SampleEntityDefinition.SampleString](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleString).

`DtoSampleBoolean` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

The value for [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

`DtoSampleInt` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The value for [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

`DtoSampleDecimal` [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

The value for [SampleEntityDefinition.SampleDecimal](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleDecimal).

## Properties

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto_DtoSampleBoolean"></a> DtoSampleBoolean

The value for [SampleEntityDefinition.SampleBoolean](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean).

```csharp
public bool DtoSampleBoolean { get; init; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto_DtoSampleDecimal"></a> DtoSampleDecimal

The value for [SampleEntityDefinition.SampleDecimal](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleDecimal).

```csharp
public decimal DtoSampleDecimal { get; init; }
```

#### Property Value

 [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto_DtoSampleInt"></a> DtoSampleInt

The value for [SampleEntityDefinition.SampleInt](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt).

```csharp
public int DtoSampleInt { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto_DtoSampleString"></a> DtoSampleString

The value for [SampleEntityDefinition.SampleString](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleString).

```csharp
public string? DtoSampleString { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

## Methods

### <a id="ONIONARCH_Application_Contracts_Dtos_CreateSampleRequestDto_MapToDomain"></a> MapToDomain\(\)

Creates a new [SampleEntityDefinition](ONIONARCH.Domain.Entities.SampleEntityDefinition.md) from this payload.
[SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId) is left at its default value.

```csharp
public SampleEntityDefinition MapToDomain()
```

#### Returns

 SampleEntityDefinition

A new, unsaved sample entity.

