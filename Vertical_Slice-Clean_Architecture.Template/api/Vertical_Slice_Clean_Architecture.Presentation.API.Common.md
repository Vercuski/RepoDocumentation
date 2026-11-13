# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Common"></a> Namespace Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common

### Classes

 [ProblemDetailsFilter](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ProblemDetailsFilter.md)

Endpoint filter, applied to every slice by [SliceRegistration.MapSlices](Vertical_Slice_Clean_Architecture.Presentation.API.Common.SliceRegistration.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_SliceRegistration_MapSlices_Microsoft_AspNetCore_Routing_IEndpointRouteBuilder_), that runs the
application's [CustomizeProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.http.problemdetailsoptions.customizeproblemdetails) on problem bodies a slice
returns itself (for example [Problems.Conflict](Vertical_Slice_Clean_Architecture.Presentation.API.Common.Problems.md#Vertical_Slice_Clean_Architecture_Presentation_API_Common_Problems_Conflict_System_String_System_String_)).

 [Problems](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.Problems.md)

Factory methods for typed RFC 9457 [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) error responses, so every slice reports errors in the same shape.

 [SliceRegistration](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.SliceRegistration.md)

Extension methods that discover, register and map vertical slices by assembly scanning.

 [ValidationFilter<TRequest\>](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ValidationFilter\-1.md)

Endpoint filter that validates the <code class="typeparamref">TRequest</code> argument with FluentValidation
before the route handler runs.

### Interfaces

 [IEndpoint](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.IEndpoint.md)

Implemented by a feature slice to register its own HTTP route(s).

 [ISliceHandler](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Common.ISliceHandler.md)

Marker interface for a feature slice's request handler.

