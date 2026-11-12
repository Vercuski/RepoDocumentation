# <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Validator"></a> Class PostSample.Validator

Namespace: [Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.md)  
Assembly: Vertical\-Slice\_Clean\-Architecture.Presentation.API.dll  

FluentValidation rules for [PostSample.Command](Vertical_Slice_Clean_Architecture.Presentation.API.Features.Sample.PostSample.Command.md), applied by <code>WithValidation&lt;Command&gt;()</code> before the handler runs.

```csharp
public sealed class PostSample.Validator : AbstractValidator<PostSample.Command>, IValidator<PostSample.Command>, IValidator, IEnumerable<IValidationRule>, IEnumerable
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
AbstractValidator<PostSample.Command\> ← 
[PostSample.Validator](Vertical\_Slice\_Clean\_Architecture.Presentation.API.Features.Sample.PostSample.Validator.md)

#### Implements

IValidator<PostSample.Command\>, 
IValidator, 
[IEnumerable<IValidationRule\>](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1), 
[IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.ienumerable)

#### Inherited Members

AbstractValidator<PostSample.Command\>.Validate\(PostSample.Command\), 
AbstractValidator<PostSample.Command\>.ValidateAsync\(PostSample.Command, CancellationToken\), 
AbstractValidator<PostSample.Command\>.Validate\(ValidationContext<PostSample.Command\>\), 
AbstractValidator<PostSample.Command\>.ValidateAsync\(ValidationContext<PostSample.Command\>, CancellationToken\), 
AbstractValidator<PostSample.Command\>.CreateDescriptor\(\), 
AbstractValidator<PostSample.Command\>.RuleFor<TProperty\>\(Expression<Func<PostSample.Command, TProperty\>\>\), 
AbstractValidator<PostSample.Command\>.RuleForEach<TElement\>\(Expression<Func<PostSample.Command, IEnumerable<TElement\>\>\>\), 
AbstractValidator<PostSample.Command\>.RuleSet\(string, Action\), 
AbstractValidator<PostSample.Command\>.When\(Func<PostSample.Command, bool\>, Action\), 
AbstractValidator<PostSample.Command\>.When\(Func<PostSample.Command, ValidationContext<PostSample.Command\>, bool\>, Action\), 
AbstractValidator<PostSample.Command\>.Unless\(Func<PostSample.Command, bool\>, Action\), 
AbstractValidator<PostSample.Command\>.Unless\(Func<PostSample.Command, ValidationContext<PostSample.Command\>, bool\>, Action\), 
AbstractValidator<PostSample.Command\>.WhenAsync\(Func<PostSample.Command, CancellationToken, Task<bool\>\>, Action\), 
AbstractValidator<PostSample.Command\>.WhenAsync\(Func<PostSample.Command, ValidationContext<PostSample.Command\>, CancellationToken, Task<bool\>\>, Action\), 
AbstractValidator<PostSample.Command\>.UnlessAsync\(Func<PostSample.Command, CancellationToken, Task<bool\>\>, Action\), 
AbstractValidator<PostSample.Command\>.UnlessAsync\(Func<PostSample.Command, ValidationContext<PostSample.Command\>, CancellationToken, Task<bool\>\>, Action\), 
AbstractValidator<PostSample.Command\>.Include\(IValidator<PostSample.Command\>\), 
AbstractValidator<PostSample.Command\>.Include<TValidator\>\(Func<PostSample.Command, TValidator\>\), 
AbstractValidator<PostSample.Command\>.GetEnumerator\(\), 
AbstractValidator<PostSample.Command\>.ClassLevelCascadeMode, 
AbstractValidator<PostSample.Command\>.RuleLevelCascadeMode, 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="Vertical_Slice_Clean_Architecture_Presentation_API_Features_Sample_PostSample_Validator__ctor"></a> Validator\(\)

Defines the rules: [SampleEntity.Id](Vertical_Slice_Clean_Architecture.Domain.Entities.SampleEntity.md#Vertical_Slice_Clean_Architecture_Domain_Entities_SampleEntity_Id) must not be [Empty](https://learn.microsoft.com/dotnet/api/system.guid.empty).

```csharp
public Validator()
```

