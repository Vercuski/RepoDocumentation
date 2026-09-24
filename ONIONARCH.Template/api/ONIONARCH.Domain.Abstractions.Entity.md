# <a id="ONIONARCH_Domain_Abstractions_Entity"></a> Class Entity

Namespace: [ONIONARCH.Domain.Abstractions](ONIONARCH.Domain.Abstractions.md)  
Assembly: ONIONARCH.Domain.dll  

Abstract base class for every persistable domain entity.

```csharp
[ExcludeFromCodeCoverage]
public abstract class Entity : IEntity
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Entity](ONIONARCH.Domain.Abstractions.Entity.md)

#### Derived

[SampleEntityDefinition](ONIONARCH.Domain.Entities.SampleEntityDefinition.md)

#### Implements

[IEntity](ONIONARCH.Domain.Abstractions.IEntity.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Serves as the generic constraint (<code>where TEntity : Entity</code>) on the Application-layer
persistence abstractions (<code>ICommandDbContext</code>, <code>IQueryDbContext</code>,
<code>IDomainMapper&lt;TEntity&gt;</code>) so only true domain entities can flow through them.
The architecture fitness tests also require every type in <code>ONIONARCH.Domain.Entities</code>
to inherit from this class and be sealed.

