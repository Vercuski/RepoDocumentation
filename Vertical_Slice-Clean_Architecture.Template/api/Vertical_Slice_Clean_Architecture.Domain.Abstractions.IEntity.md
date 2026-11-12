# <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_IEntity"></a> Interface IEntity

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Marker interface that identifies a type as a domain entity.

```csharp
public interface IEntity
```

## Remarks

It declares no members. Use it to constrain generic code (repositories, specifications,
reflection-based scanning) to domain entities only.

