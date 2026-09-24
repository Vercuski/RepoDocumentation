# <a id="ONIONARCH_Presentation_Web_Components_Pages_Error"></a> Class Error

Namespace: [ONIONARCH.Presentation.Web.Components.Pages](ONIONARCH.Presentation.Web.Components.Pages.md)  
Assembly: ONIONARCH.Presentation.Web.dll  

```csharp
[Route("/Error")]
public class Error : ComponentBase, IComponent, IHandleEvent, IHandleAfterRender
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ComponentBase](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase) ← 
[Error](ONIONARCH.Presentation.Web.Components.Pages.Error.md)

#### Implements

[IComponent](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.icomponent), 
[IHandleEvent](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.ihandleevent), 
[IHandleAfterRender](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.ihandleafterrender)

#### Inherited Members

[ComponentBase.BuildRenderTree\(RenderTreeBuilder\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.buildrendertree), 
[ComponentBase.OnInitialized\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.oninitialized), 
[ComponentBase.OnInitializedAsync\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.oninitializedasync), 
[ComponentBase.OnParametersSet\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.onparametersset), 
[ComponentBase.OnParametersSetAsync\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.onparameterssetasync), 
[ComponentBase.StateHasChanged\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.statehaschanged), 
[ComponentBase.ShouldRender\(\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.shouldrender), 
[ComponentBase.OnAfterRender\(bool\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.onafterrender), 
[ComponentBase.OnAfterRenderAsync\(bool\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.onafterrenderasync), 
[ComponentBase.InvokeAsync\(Action\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.invokeasync\#microsoft\-aspnetcore\-components\-componentbase\-invokeasync\(system\-action\)), 
[ComponentBase.InvokeAsync\(Func<Task\>\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.invokeasync\#microsoft\-aspnetcore\-components\-componentbase\-invokeasync\(system\-func\(\(system\-threading\-tasks\-task\)\)\)), 
[ComponentBase.DispatchExceptionAsync\(Exception\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.dispatchexceptionasync), 
[ComponentBase.SetParametersAsync\(ParameterView\)](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.setparametersasync), 
[ComponentBase.RendererInfo](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.rendererinfo), 
[ComponentBase.Assets](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.assets), 
[ComponentBase.AssignedRenderMode](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.componentbase.assignedrendermode), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Presentation_Web_Components_Pages_Error_BuildRenderTree_Microsoft_AspNetCore_Components_Rendering_RenderTreeBuilder_"></a> BuildRenderTree\(RenderTreeBuilder\)

Renders the component to the supplied [RenderTreeBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.rendering.rendertreebuilder).

```csharp
protected override void BuildRenderTree(RenderTreeBuilder __builder)
```

#### Parameters

`__builder` [RenderTreeBuilder](https://learn.microsoft.com/dotnet/api/microsoft.aspnetcore.components.rendering.rendertreebuilder)

### <a id="ONIONARCH_Presentation_Web_Components_Pages_Error_OnInitialized"></a> OnInitialized\(\)

Captures the request ID from the current [Activity](https://learn.microsoft.com/dotnet/api/system.diagnostics.activity), falling back to the HTTP
context's trace identifier.

```csharp
protected override void OnInitialized()
```

