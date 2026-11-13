# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample"></a> Class GetSample

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Vertical slice for <code>GET /Sample/{Id}</code>: returns a single sample by its identifier.

```csharp
public static class GetSample
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

The slice's request, response, handler and endpoint are nested in this one class. It reads
from the query (read) side of the database and projects straight into [GetSample.Response](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.GetSample.Response.md),
so no [SampleEntity](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md) is materialized and the domain type never reaches the HTTP contract.

