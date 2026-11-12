# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_ISliceHandler"></a> Interface ISliceHandler

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Marker interface for a feature slice's request handler.

```csharp
public interface ISliceHandler
```

## Remarks

[SliceRegistration.AddSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_AddSlices_Microsoft_Extensions_DependencyInjection_IServiceCollection_System_Reflection_Assembly_) registers every concrete implementation as a scoped
service under its own concrete type, so endpoints can take the handler as a parameter.

