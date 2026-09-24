# <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion"></a> Class ApplicationVersion

Namespace: [ONIONARCH.Infrastructure.Versioning](ONIONARCH.Infrastructure.Versioning.md)  
Assembly: ONIONARCH.Infrastructure.dll  

The application's semantic version, read once from the assembly metadata that MinVer
stamps at build time (see <code>Directory.Build.props</code>).

```csharp
public sealed class ApplicationVersion
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Remarks

Every project in the solution is versioned from the same git tags, so all assemblies carry the
same version. [ApplicationVersion.Current](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md#ONIONARCH_Infrastructure_Versioning_ApplicationVersion_Current) therefore reads this (Infrastructure) assembly rather than
[GetEntryAssembly](https://learn.microsoft.com/dotnet/api/system.reflection.assembly.getentryassembly), which is the test host under
<code>WebApplicationFactory</code> and would report the wrong version. Registered as a singleton by
<code>AddInfrastructureRegistration()</code>.

## Properties

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_BuildMetadata"></a> BuildMetadata

Gets the build metadata (the part after <code>+</code>), or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if there is none.

```csharp
public string? BuildMetadata { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)?

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_Current"></a> Current

The version of the running application, taken from this assembly's
[AssemblyInformationalVersionAttribute](https://learn.microsoft.com/dotnet/api/system.reflection.assemblyinformationalversionattribute).

```csharp
public static ApplicationVersion Current { get; }
```

#### Property Value

 [ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_InformationalVersion"></a> InformationalVersion

Gets the full informational version including build metadata, e.g.
<code>1.4.1-alpha.0.3+2057147a69…</code>, where the metadata is the commit SHA the .NET SDK appends.

```csharp
public string InformationalVersion { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_IsPreRelease"></a> IsPreRelease

Gets a value indicating whether this is a pre-release version (it has a <code>-</code> suffix
such as <code>-alpha.0.3</code> or <code>-rc.1</code>).

```csharp
public bool IsPreRelease { get; }
```

#### Property Value

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_SemanticVersion"></a> SemanticVersion

Gets the SemVer 2.0 version without build metadata, e.g. <code>1.4.0</code> or <code>1.4.1-alpha.0.3</code>.
This is the value to show users and compare between builds.

```csharp
public string SemanticVersion { get; }
```

#### Property Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_FromAssembly_System_Reflection_Assembly_"></a> FromAssembly\(Assembly\)

Reads the version stamped on <code class="paramref">assembly</code>.

```csharp
public static ApplicationVersion FromAssembly(Assembly assembly)
```

#### Parameters

`assembly` [Assembly](https://learn.microsoft.com/dotnet/api/system.reflection.assembly)

The assembly to read.

#### Returns

 [ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)

The version from [AssemblyInformationalVersionAttribute](https://learn.microsoft.com/dotnet/api/system.reflection.assemblyinformationalversionattribute), falling back to the
assembly version, or <code>0.0.0</code> if neither is present.

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_FromInformationalVersion_System_String_"></a> FromInformationalVersion\(string\)

Creates an instance from an informational version string.

```csharp
public static ApplicationVersion FromInformationalVersion(string informationalVersion)
```

#### Parameters

`informationalVersion` [string](https://learn.microsoft.com/dotnet/api/system.string)

The version, optionally followed by <code>+</code> and build metadata.

#### Returns

 [ApplicationVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md)

The parsed version.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

<code class="paramref">informationalVersion</code> is null, empty, or whitespace.

### <a id="ONIONARCH_Infrastructure_Versioning_ApplicationVersion_ToString"></a> ToString\(\)

Returns [ApplicationVersion.SemanticVersion](ONIONARCH.Infrastructure.Versioning.ApplicationVersion.md#ONIONARCH_Infrastructure_Versioning_ApplicationVersion_SemanticVersion).

```csharp
public override string ToString()
```

#### Returns

 [string](https://learn.microsoft.com/dotnet/api/system.string)

The semantic version string.

