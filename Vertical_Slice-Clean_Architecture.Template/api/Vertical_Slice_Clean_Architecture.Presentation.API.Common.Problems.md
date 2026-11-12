# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_Problems"></a> Class Problems

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Factory methods for typed RFC 9457 [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) error responses, so every slice reports errors in the same shape.

```csharp
public static class Problems
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[Problems](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.Problems.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_Problems_Conflict_System_String_System_String_"></a> Conflict\(string, string\)

Creates a <code>409 Conflict</code> response with a [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) body.

```csharp
public static Conflict<ProblemDetails> Conflict(string title, string detail)
```

#### Parameters

`title` [string](https://learn.microsoft.com/dotnet/api/system.string)

A short, human-readable summary of the problem.

`detail` [string](https://learn.microsoft.com/dotnet/api/system.string)

An explanation specific to this occurrence of the problem.

#### Returns

 [Conflict](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.conflict\-1)<[ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails)\>

A typed <code>409</code> result.

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common_Problems_NotFound_System_String_System_String_"></a> NotFound\(string, string\)

Creates a <code>404 Not Found</code> response with a [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) body.

```csharp
public static NotFound<ProblemDetails> NotFound(string title, string detail)
```

#### Parameters

`title` [string](https://learn.microsoft.com/dotnet/api/system.string)

A short, human-readable summary of the problem.

`detail` [string](https://learn.microsoft.com/dotnet/api/system.string)

An explanation specific to this occurrence of the problem.

#### Returns

 [NotFound](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.notfound\-1)<[ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails)\>

A typed <code>404</code> result.

