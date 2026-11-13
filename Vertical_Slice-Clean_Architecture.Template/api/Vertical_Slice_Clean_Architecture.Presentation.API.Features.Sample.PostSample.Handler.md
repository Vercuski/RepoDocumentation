# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler"></a> Class PostSample.Handler

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Adds the sample through [CommandDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.CommandDbContext.md).

```csharp
public sealed class PostSample.Handler : ISliceHandler
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[PostSample.Handler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Handler.md)

#### Implements

[ISliceHandler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ISliceHandler.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler__ctor_Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Contexts_CommandDbContext_"></a> Handler\(CommandDbContext\)

Adds the sample through [CommandDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.CommandDbContext.md).

```csharp
public Handler(CommandDbContext db)
```

#### Parameters

`db` [CommandDbContext](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts.CommandDbContext.md)

The write-side database context.

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler_Handle_Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command_System_Threading_CancellationToken_"></a> Handle\(Command, CancellationToken\)

Creates the sample unless its email address is already in use.

```csharp
public Task<Results<Created<PostSample.Response>, Conflict<ProblemDetails>>> Handle(PostSample.Command command, CancellationToken cancellationToken)
```

#### Parameters

`command` [PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md).[Command](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Command.md)

The command that holds the new sample's details.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token that cancels the database calls.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[Results](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.results\-2)<[Created](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.created\-1)<[PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md).[Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Response.md)\>, [Conflict](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.conflict\-1)<[ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails)\>\>\>

<code>201 Created</code> with a <code>Location</code> of <code>/Sample/{Id}</code>, or <code>409 Conflict</code>
with a problem body if another sample already has the email address.

#### Remarks

Two requests racing with the same email can both pass the check; the unique index on
<code>Email</code> then rejects the second save.

