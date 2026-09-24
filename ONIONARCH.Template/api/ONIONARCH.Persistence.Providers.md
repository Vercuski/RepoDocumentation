# <a id="ONIONARCH_Persistence_Providers"></a> Namespace ONIONARCH.Persistence.Providers

### Classes

 [MySQLDatabaseProvider](ONIONARCH.Persistence.Providers.MySQLDatabaseProvider.md)

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md) for MySQL. Uses the MySql.EntityFrameworkCore provider for
EF Core and MySqlConnector for Dapper connections.

 [PostgreSqlDatabaseProvider](ONIONARCH.Persistence.Providers.PostgreSqlDatabaseProvider.md)

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md) for PostgreSQL, using Npgsql for both EF Core and Dapper connections.

 [SqlServerDatabaseProvider](ONIONARCH.Persistence.Providers.SqlServerDatabaseProvider.md)

[IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md) for Microsoft SQL Server, using Microsoft.Data.SqlClient for
both EF Core and Dapper connections.

### Interfaces

 [IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

Abstracts a database platform (SQL Server, PostgreSQL, MySQL) so the EF Core and Dapper paths
can be pointed at any supported platform through configuration alone.

