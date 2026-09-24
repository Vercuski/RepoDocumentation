# <a id="ONIONARCH_Application_Abstractions_ResultErrorType"></a> Enum ResultErrorType

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Categorizes an expected business-flow failure carried by a [Result<T\>](ONIONARCH.Application.Abstractions.Result-1.md).
Presentation maps each category to an HTTP status code.

```csharp
public enum ResultErrorType
```

## Fields

`Conflict = 2` 

The request conflicts with the current state of the resource (maps to HTTP 409).



`NotFound = 0` 

The requested resource does not exist (maps to HTTP 404).



`Validation = 1` 

The request failed business validation (maps to HTTP 400).



