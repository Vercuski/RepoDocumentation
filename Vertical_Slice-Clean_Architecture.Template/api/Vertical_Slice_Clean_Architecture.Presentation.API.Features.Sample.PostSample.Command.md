# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command"></a> Class PostSample.Command

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

The request body for this slice.

```csharp
public sealed record PostSample.Command : IEquatable<PostSample.Command>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PostSample.Command](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Command.md)

#### Implements

[IEquatable<PostSample.Command\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command__ctor_System_String_System_String_"></a> Command\(string, string\)

The request body for this slice.

```csharp
public Command(string Name, string Email)
```

#### Parameters

`Name` [string](https://learn.microsoft.com/dotnet/api/system.string)

The display name of the new sample.

`Email` [string](https://learn.microsoft.com/dotnet/api/system.string)

The email address of the new sample. It must not belong to another sample.

## Properties

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command_Email"></a> Email

The email address of the new sample. It must not belong to another sample.

```csharp
public string Email { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command_Name"></a> Name

The display name of the new sample.

```csharp
public string Name { get; init; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

