# <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity"></a> Class SampleEntity

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Entities](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Example domain entity used by the <code>Sample</code> feature slices to show how an entity
moves from the domain layer, through persistence, to the API.

```csharp
public sealed record SampleEntity : IEntity, IEquatable<SampleEntity>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SampleEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.SampleEntity.md)

#### Implements

[IEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.IEntity.md), 
[IEquatable<SampleEntity\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Replace or rename this type when you build real features from the template.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Email"></a> Email

Gets or sets the email address associated with the sample.

```csharp
public required string Email { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Id"></a> Id

Gets or sets the unique identifier of the sample. The caller supplies it; the database does not generate it.

```csharp
public Guid Id { get; set; }
```

#### Property Value

 [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_IsActive"></a> IsActive

Gets or sets a value indicating whether the sample is active. Defaults to <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>.

```csharp
public bool IsActive { get; set; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Name"></a> Name

Gets or sets the display name of the sample.

```csharp
public required string Name { get; set; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

