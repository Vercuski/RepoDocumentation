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

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response__ctor_System_Guid_System_String_System_String_System_Boolean_"></a> Response\(Guid, string, string, bool\)

The response body returned when the sample is found.

```csharp
public Response(Guid Id, string Name, string Email, bool IsActive)
```

#### Parameters

`Id` [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

The identifier of the sample.

`Name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The display name of the sample.

`Email` [string](https://learn.microsoft.com/dotnet/api/system.string)

The email address of the sample.

`IsActive` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Whether the sample is active.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response_Email"></a> Email

The email address of the sample.

```csharp
public string Email { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response_Id"></a> Id

The identifier of the sample.

```csharp
public Guid Id { get; init; }
```

#### Property Value

 [Guid](https://learn.microsoft.com/dotnet/api/system.guid)

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response_IsActive"></a> IsActive

Whether the sample is active.

```csharp
public bool IsActive { get; init; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Response_Name"></a> Name

The display name of the sample.

```csharp
public string Name { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

