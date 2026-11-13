# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample"></a> Class PostSample

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Vertical slice for <code>POST /Sample</code>: creates a sample.

```csharp
public static class PostSample
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

The slice's command, response, validator, handler and endpoint are nested in this one class. It
writes to the command (write) side of the database. The request carries only what a client may
choose; the identifier and the initial state come from [SampleEntity.Create](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Create_System_String_System_String_).

