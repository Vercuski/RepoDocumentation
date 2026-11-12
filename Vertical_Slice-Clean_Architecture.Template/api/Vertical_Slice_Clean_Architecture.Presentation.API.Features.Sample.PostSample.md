# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample"></a> Class PostSample

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Vertical slice for <code>POST /Sample</code>: accepts a [SampleEntity](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md) and returns <code>201 Created</code>
when an active sample with the same identifier already exists.

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

The slice's command, response, validator, handler and endpoint are nested in this one class.

## Fields

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_MaxLines"></a> MaxLines

Maximum number of lines per request. Not currently enforced by [PostSample.Validator](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Validator.md) or used elsewhere.

```csharp
public const int MaxLines = 50
```

#### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_MaxQuantityPerLine"></a> MaxQuantityPerLine

Maximum quantity per line. Not currently enforced by [PostSample.Validator](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Validator.md) or used elsewhere.

```csharp
public const int MaxQuantityPerLine = 100
```

#### Field Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

