# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Query"></a> Class GetSample.Query

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

The request for this slice.

```csharp
public sealed record GetSample.Query : IEquatable<GetSample.Query>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSample.Query](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Query.md)

#### Implements

[IEquatable<GetSample.Query\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Query__ctor_System_Guid_"></a> Query\(Guid\)

The request for this slice.

```csharp
public Query(Guid Id)
```

#### Parameters

`Id` [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

The identifier of the sample to fetch.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Query_Id"></a> Id

The identifier of the sample to fetch.

```csharp
public Guid Id { get; init; }
```

#### Property Value

 [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

