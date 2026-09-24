# <a id="ONIONARCH_Domain_Abstractions_IBaseOptionsConfig"></a> Interface IBaseOptionsConfig

Namespace: [ONIONARCH.Domain.Abstractions](ONIONARCH.Domain.Abstractions.md)  
Assembly: ONIONARCH.Domain.dll  

Contract for strongly typed options classes that are bound from a named configuration section.

```csharp
public interface IBaseOptionsConfig
```

## Remarks

Lets the composition root discover the configuration section for an options type without
hard-coding the section name at the call site — see Persistence's <code>DependencyInjection.GetSection&lt;T&gt;</code>,
which instantiates the options type and reads [IBaseOptionsConfig.Section](ONIONARCH.Domain.Abstractions.IBaseOptionsConfig.md#ONIONARCH_Domain_Abstractions_IBaseOptionsConfig_Section) to locate its binding source.

## Properties

### <a id="ONIONARCH_Domain_Abstractions_IBaseOptionsConfig_Section"></a> Section

Gets the name of the configuration section (e.g. in <code>appsettings.json</code>) that this
options type is bound from.

```csharp
string Section { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

