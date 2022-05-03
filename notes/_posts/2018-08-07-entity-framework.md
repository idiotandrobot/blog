---
tags: Entity Framework
links:
- https://msdn.microsoft.com/en-us/library/jj193542%28v=vs.113%29.aspx?f=255&MSPPError=-2147217396
- https://stackoverflow.com/a/20184709/146360
- https://msdn.microsoft.com/en-us/library/jj591583%28v=vs.113%29.aspx?f=255&MSPPError=-2147217396
- https://stackoverflow.com/a/21885745/146360
- https://msdn.microsoft.com/en-us/library/jj200620%28v=vs.113%29.aspx?f=255&MSPPError=-2147217396
- https://stackoverflow.com/questions/20203492/entitytype-has-no-key-defined-error
- https://social.msdn.microsoft.com/Forums/en-US/648f9f5f-b844-48cb-85c3-74c8f2ee87cc/entity-framework-code-first-stop-autoincrement-and-use-my-primary-key?forum=adodotnetentityframework
- https://stackoverflow.com/questions/26303631/how-to-use-unsigned-int-long-types-with-entity-framework
---
1. EF doesn't support unsigned types. Use long for uint.
2. `[DatabaseGenerated(DatabaseGeneratedOption.None)]` attribute to turn off auto generated keys.
3. `DbContext.Table.RemoveRange(from c in DbContext.Table select c)` to clear table. Or `((IObjectContextAdapter)DbContext).ObjectContext.ExecuteStoreCommand("TRUNCATE TABLE [Table]")` for quick and dirty.
4. `[Key]` attribute to define primary key
5. Use `[Table("[Table]")]` on class for table name
