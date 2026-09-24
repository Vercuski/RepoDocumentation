# <a id="ONIONARCH_Application_Abstractions_Result_1"></a> Struct Result<T\>

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Outcome of a request handler: either a successful value or an expected business-flow failure.

```csharp
public readonly struct Result<T>
```

#### Type Parameters

`T` 

The type of the success value.

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Use this only for failures that are part of normal business flow (not found, validation,
conflict). Genuine infrastructure exceptions should propagate so the global exception handler
can log them and return a 500 response, rather than being hidden inside a failed result.

## Properties

### <a id="ONIONARCH_Application_Abstractions_Result_1_Error"></a> Error

Gets a description of the failure, or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> when [Result.IsSuccess](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_IsSuccess) is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>.

```csharp
public string? Error { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

### <a id="ONIONARCH_Application_Abstractions_Result_1_ErrorType"></a> ErrorType

Gets the failure category. Only meaningful when [Result.IsSuccess](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_IsSuccess) is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>;
on success it holds the enum's default value.

```csharp
public ResultErrorType ErrorType { get; }
```

#### Property Value

 [ResultErrorType](ONIONARCH.Application.Abstractions.ResultErrorType.md)

### <a id="ONIONARCH_Application_Abstractions_Result_1_IsSuccess"></a> IsSuccess

Gets a value indicating whether the operation succeeded.

```csharp
public bool IsSuccess { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Application_Abstractions_Result_1_Value"></a> Value

Gets the success value, or the default of <code class="typeparamref">T</code> when [Result.IsSuccess](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_IsSuccess) is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

```csharp
public T? Value { get; }
```

#### Property Value

 T?

## Methods

### <a id="ONIONARCH_Application_Abstractions_Result_1_Failure_System_String_ONIONARCH_Application_Abstractions_ResultErrorType_"></a> Failure\(string, ResultErrorType\)

Creates a failed result.

```csharp
public static Result<T> Failure(string error, ResultErrorType errorType)
```

#### Parameters

`error` [string](https://learn.microsoft.com/dotnet/api/system.string)

A description of the failure, suitable for returning to the caller.

`errorType` [ResultErrorType](ONIONARCH.Application.Abstractions.ResultErrorType.md)

The failure category.

#### Returns

 [Result](ONIONARCH.Application.Abstractions.Result\-1.md)<T\>

A result whose [Result.IsSuccess](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_IsSuccess) is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

### <a id="ONIONARCH_Application_Abstractions_Result_1_Success__0_"></a> Success\(T\)

Creates a successful result carrying <code class="paramref">value</code>.

```csharp
public static Result<T> Success(T value)
```

#### Parameters

`value` T

The success value.

#### Returns

 [Result](ONIONARCH.Application.Abstractions.Result\-1.md)<T\>

A result whose [Result.IsSuccess](ONIONARCH.Application.Abstractions.Result-1.md#ONIONARCH_Application_Abstractions_Result_1_IsSuccess) is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a>.

