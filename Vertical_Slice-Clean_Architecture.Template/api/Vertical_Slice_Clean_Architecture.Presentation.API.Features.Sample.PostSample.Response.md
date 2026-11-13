# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Response"></a> Class PostSample.Response

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

The response body returned on success.

```csharp
public sealed record PostSample.Response : IEquatable<PostSample.Response>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PostSample.Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Response.md)

#### Implements

[IEquatable<PostSample.Response\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Response__ctor_System_Guid_"></a> Response\(Guid\)

The response body returned on success.

```csharp
public Response(Guid Id)
```

#### Parameters

`Id` [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

The identifier the server assigned to the new sample.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Response_Id"></a> Id

The identifier the server assigned to the new sample.

```csharp
public Guid Id { get; init; }
```

#### Property Value

 [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

