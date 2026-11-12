# <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_Entity"></a> Class Entity

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Optional abstract base class for domain entities that are modelled as classes.

```csharp
[ExcludeFromCodeCoverage]
public abstract class Entity : IEntity
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Entity](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.Entity.md)

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

It carries no state or behavior yet. It exists as a single place to add members that every
class-based entity should share (for example an identifier, audit fields or domain events).
Entities written as records, such as <code>SampleEntity</code>, implement [IEntity](Vertical_Slice_Clean_Architecture.Domain.Abstractions.IEntity.md) directly instead.

