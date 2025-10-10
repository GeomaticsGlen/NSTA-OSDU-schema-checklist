## 🔧 Core OSDU Storage API Endpoints

|Endpoint|Method|Purpose|Priority|
|---|---|---|---|
|`/records`|`PUT`|Ingest one or more records|✅ Already implemented|
|`/records/{id}`|`GET`|Retrieve a record by ID|🔼 High — needed for validation/audit|
|`/records/{id}`|`DELETE`|Delete a record|🔼 High — cleanup and rollback|
|`/records/{id}`|`PATCH`|Update a record|🔼 High — if schema supports partial updates|
|`/records:batch`|`POST`|Bulk ingestion|🔼 High — for performance testing|
|`/records:delete`|`POST`|Bulk delete by ID list|🔼 High — complements batch ingestion|
|`/records:retrieve`|`POST`|Bulk retrieve by ID list|🔼 High — for audit and validation|
|`/query`|`POST`|Search records using query DSL|⚠️ Medium — depends on indexing strategy|
|`/schemas/{schemaId}`|`GET`|Retrieve schema definition|⚠️ Medium — useful for validation|
|`/schemas`|`POST`|Register a new schema|⚠️ Medium — if dynamic schema registration is needed|

## 🧭 Suggested Implementation Order

1. `GET /records/{id}` — validate inserts
    
2. `POST /records:batch` — enable bulk ingestion
    
3. `POST /records:retrieve` — audit multiple records
    
4. `DELETE /records/{id}` — support cleanup
    
5. `POST /records:delete` — bulk cleanup
    
6. `PATCH /records/{id}` — enable updates
    
7. `POST /query` — enable search
    
8. `GET /schemas/{schemaId}` — introspect schema
    
9. `POST /schemas` — register new schema