# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler"></a> Class PostSample.Handler

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Processes a [PostSample.Command](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md) against [SampleDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Contexts.SampleDbContext.md).

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

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler__ctor_Vertical_Slice_Clean_Architecture_Infrastructure_Contexts_SampleDbContext_"></a> Handler\(SampleDbContext\)

Processes a [PostSample.Command](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md) against [SampleDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Contexts.SampleDbContext.md).

```csharp
public Handler(SampleDbContext db)
```

#### Parameters

`db` SampleDbContext

The database context to read from and save to.

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Handler_Handle_Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command_System_Threading_CancellationToken_"></a> Handle\(Command, CancellationToken\)

Checks that an active sample with the submitted identifier exists, then saves pending changes.

```csharp
public Task<Results<Created<PostSample.Response>, NotFound<ProblemDetails>, Conflict<ProblemDetails>>> Handle(PostSample.Command command, CancellationToken cancellationToken)
```

#### Parameters

`command` [PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md).[Command](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Command.md)

The command that holds the submitted sample.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token that cancels the database calls.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[Results](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.results\-3)<[Created](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.created\-1)<[PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md).[Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Response.md)\>, [NotFound](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.notfound\-1)<[ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails)\>, [Conflict](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.conflict\-1)<[ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails)\>\>\>

<ul><li><code>404 Not Found</code> with a problem body if no active sample with that identifier exists.</li><li><code>409 Conflict</code> with a problem body if the save fails with a [DbUpdateConcurrencyException](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbupdateconcurrencyexception).</li><li>Otherwise <code>201 Created</code> with a <code>Location</code> of <code>/Sample/{Id}</code> and a [PostSample.Response](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Response.md) body.</li></ul>

#### Remarks

The handler does not add [PostSample.Command.Sample](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md#Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Command_Sample) to the context, so <code>SaveChangesAsync</code>
currently has nothing to save.

