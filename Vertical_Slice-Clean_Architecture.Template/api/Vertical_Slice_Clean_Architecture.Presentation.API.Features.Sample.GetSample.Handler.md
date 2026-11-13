# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Handler"></a> Class GetSample.Handler

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

Runs the query against [QueryDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.QueryDbContext.md).

```csharp
public sealed class GetSample.Handler : ISliceHandler
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSample.Handler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Handler.md)

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

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Handler__ctor_Vertical_Slice_Clean_Architecture_Infrastructure_Persistence_Contexts_QueryDbContext_"></a> Handler\(QueryDbContext\)

Runs the query against [QueryDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Persistence.Contexts.QueryDbContext.md).

```csharp
public Handler(QueryDbContext db)
```

#### Parameters

`db` [QueryDbContext](Vertical\_Slice\_Clean\_Architecture.Infrastructure.Persistence.Contexts.QueryDbContext.md)

The read-side database context.

## Methods

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Handler_Handle_Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_GetSample_Query_System_Threading_CancellationToken_"></a> Handle\(Query, CancellationToken\)

Looks up the sample with the requested identifier, selecting only the columns the response needs.

```csharp
public Task<Results<Ok<GetSample.Response>, NotFound>> Handle(GetSample.Query query, CancellationToken cancellationToken)
```

#### Parameters

`query` [GetSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.md).[Query](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Query.md)

The query that holds the identifier to look up.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token that cancels the database call.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[Results](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.results\-2)<[Ok](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.ok\-1)<[GetSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.md).[Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Response.md)\>, [NotFound](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.httpresults.notfound)\>\>

<code>200 OK</code> with a [GetSample.Response](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.GetSample.Response.md) if the sample exists; otherwise <code>404 Not Found</code>.

