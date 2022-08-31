# Idempotent SQL
## Insert
Options
- Check for existence first
- Delete, then insert (will fail if foreign keys depend on it)


## Upsert
Do an update to an existing item, or an insert if it doesn't exist yet.  
This can be done with a try/catch - the insert is done in the try, and the update is done in the catch.  
