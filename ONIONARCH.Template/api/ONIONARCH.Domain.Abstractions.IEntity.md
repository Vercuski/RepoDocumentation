# <a id="ONIONARCH_Domain_Abstractions_IEntity"></a> Interface IEntity

Namespace: [ONIONARCH.Domain.Abstractions](ONIONARCH.Domain.Abstractions.md)  
Assembly: ONIONARCH.Domain.dll  

Marker interface identifying a type as a domain entity.

```csharp
public interface IEntity
```

## Remarks

Carries no members; concrete entities should derive from [Entity](ONIONARCH.Domain.Abstractions.Entity.md), which
implements this interface, rather than implementing it directly.

