# <a id="ONIONARCH_Infrastructure_Exceptions"></a> Namespace ONIONARCH.Infrastructure.Exceptions

### Classes

 [GlobalExceptionHandler](ONIONARCH.Infrastructure.Exceptions.GlobalExceptionHandler.md)

Centralized handler for unhandled exceptions in every web host. Logs the exception and
returns an RFC 7807 [ProblemDetails](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.problemdetails) 500 response that includes the request's
correlation ID, without leaking exception details to the caller.

