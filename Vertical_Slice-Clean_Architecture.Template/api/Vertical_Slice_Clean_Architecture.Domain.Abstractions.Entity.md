# <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_Entity"></a> Class Entity

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Abstract base class for domain entities: every entity has a [Entity.Id](Vertical_Slice_Clean_Architecture.Domain.Abstractions.Entity.md#Vertical_Slice_Clean_Architecture_Domain_Abstractions_Entity_Id) that identifies it.

```csharp
[ExcludeFromCodeCoverage]
public abstract class Entity : IEntity
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Entity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.Entity.md)

#### Derived

[SampleEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Entities.SampleEntity.md)

#### Implements

[IEntity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.IEntity.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

<p>
Add members here that every entity should share, for example audit fields or domain events.
</p>
<p>
[Entity.Id](Vertical_Slice_Clean_Architecture.Domain.Abstractions.Entity.md#Vertical_Slice_Clean_Architecture_Domain_Abstractions_Entity_Id) has a protected setter, so only the entity itself (typically in a factory
method) assigns it. EF Core and Dapper can still set it when they load a row, because both
write to non-public setters.
</p>

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_Entity_Id"></a> Id

Gets the unique identifier of the entity.

```csharp
public Guid Id { get; protected set; }
```

#### Property Value

 [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

