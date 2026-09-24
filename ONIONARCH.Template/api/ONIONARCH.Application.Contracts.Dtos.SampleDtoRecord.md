# <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord"></a> Class SampleDtoRecord

Namespace: [ONIONARCH.Application.Contracts.Dtos](ONIONARCH.Application.Contracts.Dtos.md)  
Assembly: ONIONARCH.Application.dll  

Outbound representation of a sample entity returned to API callers.

```csharp
public sealed record SampleDtoRecord : IEquatable<SampleDtoRecord>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SampleDtoRecord](ONIONARCH.Application.Contracts.Dtos.SampleDtoRecord.md)

#### Implements

[IEquatable<SampleDtoRecord\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord__ctor_System_Int32_"></a> SampleDtoRecord\(int\)

Outbound representation of a sample entity returned to API callers.

```csharp
public SampleDtoRecord(int Id)
```

#### Parameters

`Id` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The entity's key, taken from [SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId).

## Properties

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_DtoSampleBoolean"></a> DtoSampleBoolean

Gets the sample Boolean value.

```csharp
public bool DtoSampleBoolean { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_DtoSampleDecimal"></a> DtoSampleDecimal

Gets the sample decimal value.

```csharp
public decimal DtoSampleDecimal { get; }
```

#### Property Value

 [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_DtoSampleId"></a> DtoSampleId

Gets the sample identifier.

```csharp
public int DtoSampleId { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

#### Remarks

[SampleDtoRecord.Create](ONIONARCH.Application.Contracts.Dtos.SampleDtoRecord.md#ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_Create_ONIONARCH_Domain_Entities_SampleEntityDefinition_) does not currently assign this property, so it serializes as <code>0</code>;
the entity's key is carried by [SampleDtoRecord.Id](ONIONARCH.Application.Contracts.Dtos.SampleDtoRecord.md#ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_Id).

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_DtoSampleInt"></a> DtoSampleInt

Gets the sample integer value.

```csharp
public int DtoSampleInt { get; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_DtoSampleString"></a> DtoSampleString

Gets the sample string value.

```csharp
public string? DtoSampleString { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_Id"></a> Id

The entity's key, taken from [SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId).

```csharp
public int Id { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Methods

### <a id="ONIONARCH_Application_Contracts_Dtos_SampleDtoRecord_Create_ONIONARCH_Domain_Entities_SampleEntityDefinition_"></a> Create\(SampleEntityDefinition\)

Creates a DTO from a domain entity.

```csharp
public static SampleDtoRecord Create(SampleEntityDefinition entity)
```

#### Parameters

`entity` SampleEntityDefinition

The entity to project.

#### Returns

 [SampleDtoRecord](ONIONARCH.Application.Contracts.Dtos.SampleDtoRecord.md)

A new [SampleDtoRecord](ONIONARCH.Application.Contracts.Dtos.SampleDtoRecord.md) populated from <code class="paramref">entity</code>.

