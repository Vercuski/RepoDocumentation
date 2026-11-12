# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response"></a> Class GetSample.Response

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

The response body returned when the sample is found.

```csharp
public sealed record GetSample.Response : IEquatable<GetSample.Response>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSample.Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Response.md)

#### Implements

[IEquatable<GetSample.Response\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response__ctor_System_Collections_Generic_IList_Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity__"></a> Response\(IList<SampleEntity\>\)

The response body returned when the sample is found.

```csharp
public Response(IList<SampleEntity> Samples)
```

#### Parameters

`Samples` [IList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ilist\-1)<SampleEntity\>

The matching samples. It contains exactly one item when returned by [GetSample.Handler](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.GetSample.Handler.md).

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response_Samples"></a> Samples

The matching samples. It contains exactly one item when returned by [GetSample.Handler](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.GetSample.Handler.md).

```csharp
public IList<SampleEntity> Samples { get; init; }
```

#### Property Value

 [IList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ilist\-1)<SampleEntity\>

