# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample"></a> Namespace Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample

### Classes

 [PostSample.Command](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Command.md)

The request body for this slice.

 [PostSample.Endpoint](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Endpoint.md)

Registers the <code>POST /Sample</code> route for this slice.

 [GetSample.Endpoint](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Endpoint.md)

Registers the <code>GET /Sample/{Id:guid}</code> route for this slice.

 [GetSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.md)

Vertical slice for <code>GET /Sample/{Id}</code>: returns a single [SampleEntity](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md) by its identifier.

 [PostSample.Handler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Handler.md)

Processes a [PostSample.Command](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md) against [SampleDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Contexts.SampleDbContext.md).

 [GetSample.Handler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Handler.md)

Runs the query against [SampleDbContext](Vertical_Slice_Clean_Architecture.Infrastructure.Contexts.SampleDbContext.md).

 [PostSample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.md)

Vertical slice for <code>POST /Sample</code>: accepts a [SampleEntity](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md) and returns <code>201 Created</code>
when an active sample with the same identifier already exists.

 [GetSample.Query](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Query.md)

The request for this slice.

 [GetSample.Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.GetSample.Response.md)

The response body returned when the sample is found.

 [PostSample.Response](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Response.md)

The response body returned on success.

 [PostSample.Validator](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Validator.md)

FluentValidation rules for [PostSample.Command](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md), applied by <code>WithValidation&lt;Command&gt;()</code> before the handler runs.

