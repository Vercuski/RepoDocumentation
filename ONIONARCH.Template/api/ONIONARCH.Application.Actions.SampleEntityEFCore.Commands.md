# <a id="ONIONARCH_Application_Actions_SampleEntityEFCore_Commands"></a> Namespace ONIONARCH.Application.Actions.SampleEntityEFCore.Commands

### Classes

 [BulkCreateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkCreateSampleEntityEFCoreRequest.md)

Command to insert many sample entities in one bulk operation through the EF Core bulk port.

 [BulkDeleteSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkDeleteSampleEntityEFCoreRequest.md)

Command to delete many sample entities with one set-based <code>DELETE</code> through the EF Core bulk
port ([IBulkCommandDbContext.DeleteWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_DeleteWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

 [BulkUpdateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkUpdateSampleEntityEFCoreRequest.md)

Command to update many sample entities with one set-based <code>UPDATE</code> through the EF Core bulk
port ([IBulkCommandDbContext.UpdateWhereAsync<TEntity\>](ONIONARCH.Application.Abstractions.Context.IBulkCommandDbContext.md#ONIONARCH_Application_Abstractions_Context_IBulkCommandDbContext_UpdateWhereAsync__1_System_Linq_Expressions_Expression_System_Func___0_System_Boolean___System_Action_ONIONARCH_Application_Abstractions_Context_IBulkUpdateSetters___0___System_Threading_CancellationToken_)), without loading them. Works on
every database platform.

 [BulkUpsertSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.BulkUpsertSampleEntityEFCoreRequest.md)

Command to insert or update many sample entities by key in one bulk operation through the EF Core
bulk port.

 [CreateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.CreateSampleEntityEFCoreRequest.md)

Command to insert a new sample entity through the EF Core persistence path.

 [DeleteSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.DeleteSampleEntityEFCoreRequest.md)

Command to delete a sample entity through the EF Core persistence path.

 [UpdateSampleEntityEFCoreRequest](ONIONARCH.Application.Actions.SampleEntityEFCore.Commands.UpdateSampleEntityEFCoreRequest.md)

Command to update an existing sample entity through the EF Core persistence path.

