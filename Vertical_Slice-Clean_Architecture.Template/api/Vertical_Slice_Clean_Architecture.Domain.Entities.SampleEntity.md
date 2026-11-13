# <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity"></a> Class SampleEntity

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Entities](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Example domain entity used by the <code>Sample</code> feature slices to show how an entity moves from
the domain layer, through persistence, to the API.

```csharp
public sealed class SampleEntity : Entity, IEntity
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Entity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.Entity.md) ← 
[SampleEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.SampleEntity.md)

#### Implements

[IEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.IEntity.md)

#### Inherited Members

[Entity.Id](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.Entity.md\#Vertical\_Slice\_Clean\_Architecture\_Domain\_Abstractions\_Entity\_Id), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
State changes only through the entity's own members ([SampleEntity.Create](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Create_System_String_System_String_), [SampleEntity.Deactivate](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Deactivate)),
so it can never hold invalid values. The API never exposes it directly: slices accept and return
their own request and response types.
</p>
<p>
Replace or rename this type when you build real features from the template.
</p>

## Fields

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_EmailMaxLength"></a> EmailMaxLength

The maximum length of [SampleEntity.Email](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Email) (the longest valid email address), shared by the
database mapping and request validation.

```csharp
public const int EmailMaxLength = 320
```

#### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_NameMaxLength"></a> NameMaxLength

The maximum length of [SampleEntity.Name](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Name), shared by the database mapping and request validation.

```csharp
public const int NameMaxLength = 200
```

#### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Email"></a> Email

Gets the email address of the sample. It is unique across all samples.

```csharp
public string Email { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_IsActive"></a> IsActive

Gets a value indicating whether the sample is active. New samples are active.

```csharp
public bool IsActive { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Name"></a> Name

Gets the display name of the sample.

```csharp
public string Name { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Create_System_String_System_String_"></a> Create\(string, string\)

Creates a new, active sample with a new time-ordered identifier (UUID version 7, which keeps
primary-key inserts sequential).

```csharp
public static SampleEntity Create(string name, string email)
```

#### Parameters

`name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The display name, at most [SampleEntity.NameMaxLength](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_NameMaxLength) characters.

`email` [string](https://learn.microsoft.com/dotnet/api/system.string)

The email address, at most [SampleEntity.EmailMaxLength](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_EmailMaxLength) characters.

#### Returns

 [SampleEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.SampleEntity.md)

The new sample.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

<code class="paramref">name</code> or <code class="paramref">email</code> is null, empty, whitespace, or too long.

### <a id="Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Deactivate"></a> Deactivate\(\)

Marks the sample as inactive.

```csharp
public void Deactivate()
```

