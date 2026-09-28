# <a id="ONIONARCH_Persistence"></a> Namespace ONIONARCH.Persistence

### Namespaces

 [ONIONARCH.Persistence.ConnectionFactory](ONIONARCH.Persistence.ConnectionFactory.md)

 [ONIONARCH.Persistence.Contexts](ONIONARCH.Persistence.Contexts.md)

 [ONIONARCH.Persistence.MySql](ONIONARCH.Persistence.MySql.md)

 [ONIONARCH.Persistence.Options](ONIONARCH.Persistence.Options.md)

 [ONIONARCH.Persistence.PostgreSql](ONIONARCH.Persistence.PostgreSql.md)

 [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)

 [ONIONARCH.Persistence.Repositories](ONIONARCH.Persistence.Repositories.md)

 [ONIONARCH.Persistence.SqlServer](ONIONARCH.Persistence.SqlServer.md)

### Classes

 [DependencyInjection](ONIONARCH.Persistence.DependencyInjection.md)

Composition-root extensions that register the Persistence layer: configuration options,
the database provider for each side of the CQRS split (resolved from the providers the host
registers in a [DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)), and both the Dapper and EF Core
implementations of the Application-layer persistence ports.

