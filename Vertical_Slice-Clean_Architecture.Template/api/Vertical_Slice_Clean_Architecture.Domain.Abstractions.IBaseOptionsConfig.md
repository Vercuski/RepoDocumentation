# <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_IBaseOptionsConfig"></a> Interface IBaseOptionsConfig

Namespace: [Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions](Vertical\_Slice\_Clean\_Architecture.Domain.Abstractions.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Domain.dll  

Contract for strongly typed options classes that are bound from application configuration.

```csharp
public interface IBaseOptionsConfig
```

## Remarks

Implementations name the configuration section they bind to, so that registration code can
bind any options type generically (for example
<code>services.Configure&lt;TOptions&gt;(configuration.GetSection(options.Section))</code>)
without hard-coding section names.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Domain_Abstractions_IBaseOptionsConfig_Section"></a> Section

Gets the name of the configuration section (for example in <code>appsettings.json</code>)
that this options type is bound from.

```csharp
string Section { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

