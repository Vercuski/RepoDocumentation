# <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition"></a> Class SampleEntityDefinition

Namespace: [ONIONARCH.Domain.Entities](ONIONARCH.Domain.Entities.md)  
Assembly: ONIONARCH.Domain.dll  

Sample domain entity used to demonstrate both the EF Core and Dapper persistence paths
end to end. Replace or extend it with real entities when building on this template.

```csharp
[ExcludeFromCodeCoverage]
public sealed class SampleEntityDefinition : Entity, IEntity
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Entity](ONIONARCH.Domain.Abstractions.Entity.md) ← 
[SampleEntityDefinition](ONIONARCH.Domain.Entities.SampleEntityDefinition.md)

#### Implements

[IEntity](ONIONARCH.Domain.Abstractions.IEntity.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleBoolean"></a> SampleBoolean

Gets or sets a sample Boolean value.

```csharp
public bool SampleBoolean { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleDecimal"></a> SampleDecimal

Gets or sets a sample decimal value.

```csharp
public decimal SampleDecimal { get; set; }
```

#### Property Value

 [decimal](https://learn.microsoft.com/dotnet/api/system.decimal)

### <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId"></a> SampleId

Gets or sets the primary key of the sample entity.

```csharp
[Key]
public int SampleId { get; set; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleInt"></a> SampleInt

Gets or sets a sample integer value.

```csharp
public int SampleInt { get; set; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleString"></a> SampleString

Gets or sets a required sample string value.

```csharp
[Required]
public string? SampleString { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

