# <a id="ONIONARCH_Presentation_API_Extensions_ResultExtensions"></a> Class ResultExtensions

Namespace: [ONIONARCH.Presentation.API.Extensions](ONIONARCH.Presentation.API.Extensions.md)  
Assembly: ONIONARCH.Presentation.API.dll  

Maps Application-layer [Result<T\>](ONIONARCH.Application.Abstractions.Result-1.md) values to MVC [IActionResult](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.iactionresult)s so
controllers share one consistent status-code mapping.

```csharp
public static class ResultExtensions
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ResultExtensions](ONIONARCH.Presentation.API.Extensions.ResultExtensions.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Failure mapping: [ResultErrorType.NotFound](ONIONARCH.Application.Abstractions.ResultErrorType.md) → 404,
[ResultErrorType.Validation](ONIONARCH.Application.Abstractions.ResultErrorType.md) → 400, [ResultErrorType.Conflict](ONIONARCH.Application.Abstractions.ResultErrorType.md) → 409,
anything else → 500 problem details.

## Methods

### <a id="ONIONARCH_Presentation_API_Extensions_ResultExtensions_ToActionResult__1_ONIONARCH_Application_Abstractions_Result___0__Microsoft_AspNetCore_Mvc_ControllerBase_"></a> ToActionResult<T\>\(Result<T\>, ControllerBase\)

Maps a [Result<T\>](ONIONARCH.Application.Abstractions.Result-1.md) directly to an [IActionResult](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.iactionresult).
On success, returns 200 OK with <code>result.Value</code> as-is.

```csharp
public static IActionResult ToActionResult<T>(this Result<T> result, ControllerBase controller)
```

#### Parameters

`result` Result<T\>

The handler result to map.

`controller` [ControllerBase](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.controllerbase)

The controller used to create the response.

#### Returns

 [IActionResult](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.iactionresult)

200 OK on success; otherwise the error response for [Result.ErrorType](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_ErrorType).

#### Type Parameters

`T` 

The type of the success value.

### <a id="ONIONARCH_Presentation_API_Extensions_ResultExtensions_ToActionResult__2_ONIONARCH_Application_Abstractions_Result___0__Microsoft_AspNetCore_Mvc_ControllerBase_System_Func___0___1__"></a> ToActionResult<T, TResponse\>\(Result<T\>, ControllerBase, Func<T, TResponse\>\)

Maps a [Result<T\>](ONIONARCH.Application.Abstractions.Result-1.md) to an [IActionResult](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.iactionresult), projecting the
success value through <code class="paramref">onSuccess</code> (e.g. entity -&gt; DTO) before
returning it via 200 OK. Mirrors the original controller behavior of treating a
success with a null value as not-found.

```csharp
public static IActionResult ToActionResult<T, TResponse>(this Result<T> result, ControllerBase controller, Func<T, TResponse> onSuccess)
```

#### Parameters

`result` Result<T\>

The handler result to map.

`controller` [ControllerBase](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.controllerbase)

The controller used to create the response.

`onSuccess` [Func](https://learn.microsoft.com/dotnet/api/system.func\-2)<T, TResponse\>

Projects the success value into the response body.

#### Returns

 [IActionResult](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.iactionresult)

200 OK with the projected value on success; otherwise the mapped error response.

#### Type Parameters

`T` 

The type of the success value.

`TResponse` 

The type returned to the caller.

#### Remarks

A success with a <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> value falls through to the error mapping; because
[Result.ErrorType](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_ErrorType) defaults to [ResultErrorType.NotFound](ONIONARCH.Application.Abstractions.ResultErrorType.md), that yields 404.

