# <a id="ONIONARCH_Persistence_Providers"></a> Namespace ONIONARCH.Persistence.Providers

### Classes

 [DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)

Composition-root registry of the database providers a host has opted into. Each provider project
contributes an extension method (<code>AddSqlServer</code>, <code>AddPostgreSql</code>, <code>AddMySql</code>) that
adds its provider here, so the core Persistence project resolves providers by configured platform
key without a compile-time dependency on any of them.

### Interfaces

 [IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

Abstracts a database platform so the EF Core and Dapper paths can be pointed at any supported
platform through configuration alone. Implemented by the provider-specific projects
(ONIONARCH.Persistence.SqlServer, .PostgreSql, .MySql); this core project owns the contract but
never references a concrete provider. Hosts opt providers in through
[DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md).

