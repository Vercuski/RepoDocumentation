# <a id="ONIONARCH_Application_Abstractions_IDomainMapper_1"></a> Interface IDomainMapper<TEntity\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Implemented by inbound DTOs that know how to convert themselves into a domain entity.

```csharp
public interface IDomainMapper<out TEntity> where TEntity : Entity
```

#### Type Parameters

`TEntity` 

The domain entity type the DTO maps to.

## Methods

### <a id="ONIONARCH_Application_Abstractions_IDomainMapper_1_MapToDomain"></a> MapToDomain\(\)

Creates a new domain entity populated from this DTO's values.

```csharp
TEntity MapToDomain()
```

#### Returns

 TEntity

A new <code class="typeparamref">TEntity</code> instance.

