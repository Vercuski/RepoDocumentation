# <a id="ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters_1"></a> Interface IBulkUpdateSetters<TEntity\>

Namespace: [ONIONARCH.Application.Abstractions.Context](ONIONARCH.Application.Abstractions.Context.md)  
Assembly: ONIONARCH.Application.dll  

Declares the column assignments of a set-based update issued through
[IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_). Each call adds one <code>SET</code> clause.

```csharp
public interface IBulkUpdateSetters<TEntity> where TEntity : Entity
```

#### Type Parameters

`TEntity` 

The domain entity type being updated.

## Remarks

Mirrors EF Core's <code>UpdateSettersBuilder&lt;T&gt;</code> so the Application layer can describe an
update without referencing EF Core. Calls may be made conditionally (e.g. only set a column when a
request field is supplied); the Persistence implementation forwards each one as it is made.

## Methods

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters_1_Set__1_System_Linq_Expressions_Expression_System_Func__0___0_____0_"></a> Set<TProperty\>\(Expression<Func<TEntity, TProperty\>\>, TProperty\)

Sets <code class="paramref">property</code> to a constant <code class="paramref">value</code> (sent as a parameter).

```csharp
IBulkUpdateSetters<TEntity> Set<TProperty>(Expression<Func<TEntity, TProperty>> property, TProperty value)
```

#### Parameters

`property` [Expression](https://learn.microsoft.com/dotnet/api/system.linq.expressions.expression\-1)<[Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TEntity, TProperty\>\>

Selects the mapped property to set, e.g. <code>e =&gt; e.Name</code>.

`value` TProperty

The value to assign.

#### Returns

 [IBulkUpdateSetters](ONIONARCH.Application.Abstractions.Context.IBulkUpdateSetters\-1.md)<TEntity\>

This instance, for chaining.

#### Type Parameters

`TProperty` 

The property type.

### <a id="ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters_1_Set__1_System_Linq_Expressions_Expression_System_Func__0___0___System_Linq_Expressions_Expression_System_Func__0___0___"></a> Set<TProperty\>\(Expression<Func<TEntity, TProperty\>\>, Expression<Func<TEntity, TProperty\>\>\)

Sets <code class="paramref">property</code> to a value computed in SQL from the current row,
e.g. <code>e =&gt; e.Count + 1</code>.

```csharp
IBulkUpdateSetters<TEntity> Set<TProperty>(Expression<Func<TEntity, TProperty>> property, Expression<Func<TEntity, TProperty>> value)
```

#### Parameters

`property` [Expression](https://learn.microsoft.com/dotnet/api/system.linq.expressions.expression\-1)<[Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TEntity, TProperty\>\>

Selects the mapped property to set.

`value` [Expression](https://learn.microsoft.com/dotnet/api/system.linq.expressions.expression\-1)<[Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<TEntity, TProperty\>\>

An expression over the current row that must be translatable to SQL.

#### Returns

 [IBulkUpdateSetters](ONIONARCH.Application.Abstractions.Context.IBulkUpdateSetters\-1.md)<TEntity\>

This instance, for chaining.

#### Type Parameters

`TProperty` 

The property type.

