# <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Queries_GetSingleSampleEntityDapperRequest"></a> Class GetSingleSampleEntityDapperRequest

Namespace: [ONIONARCH.Application.Actions.SampleEntityDapper.Queries](ONIONARCH.Application.Actions.SampleEntityDapper.Queries.md)  
Assembly: ONIONARCH.Application.dll  

Query to retrieve a single sample entity by key through the Dapper persistence path.

```csharp
public sealed record GetSingleSampleEntityDapperRequest : IQueryRequest<Result<SampleEntityDefinition>>, IAppRequest<Result<SampleEntityDefinition>>, IEquatable<GetSingleSampleEntityDapperRequest>
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[GetSingleSampleEntityDapperRequest](ONIONARCH.Application.Actions.SampleEntityDapper.Queries.GetSingleSampleEntityDapperRequest.md)

#### Implements

[IQueryRequest<Result<SampleEntityDefinition\>\>](ONIONARCH.Application.Abstractions.IQueryRequest\-1.md), 
[IAppRequest<Result<SampleEntityDefinition\>\>](ONIONARCH.Application.Abstractions.IAppRequest\-1.md), 
[IEquatable<GetSingleSampleEntityDapperRequest\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Queries_GetSingleSampleEntityDapperRequest__ctor_System_Int32_"></a> GetSingleSampleEntityDapperRequest\(int\)

Query to retrieve a single sample entity by key through the Dapper persistence path.

```csharp
public GetSingleSampleEntityDapperRequest(int Id)
```

#### Parameters

`Id` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the entity to retrieve.

## Properties

### <a id="ONIONARCH_Application_Actions_SampleEntityDapper_Queries_GetSingleSampleEntityDapperRequest_Id"></a> Id

The key of the entity to retrieve.

```csharp
public int Id { get; init; }
```

#### Property Value

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

