
open-test-data\rc--3.0.0\readme
🔑 Key Implications of the README

1. **Reference Values are First‑Class Data**
    
    - The repo isn’t just “example wells” — it includes **reference data** (countries, units of measure, statuses, etc.) that other records depend on.
        
    - Implication: you must load these **reference manifests first** (before wells, wellbores, seismic, etc.), otherwise downstream records will fail validation because they point to reference values that don’t exist.
        
2. **IDs are Deterministic**
    
    - IDs are generated from `data.Code` using URL encoding rules:
        
        Code
        
        ```
        {{data-partition-id}}:reference-data--ReferenceDataType:encodedCode
        ```
        
    - Implication: your local environment must accept these IDs as‑is. Don’t rewrite them. Instead, configure your Storage/Schema services to accept the `opendes` partition and the encoded IDs.
        
3. **Partition Awareness**
    
    - The manifests assume a partition like `opendes`.
        
    - Implication: your local services must recognise `data-partition-id: opendes` in headers. If you force `osdu-local`, you’ll break compatibility. Better to configure your environment to accept `opendes`.
        
4. **Legal & ACL Dependencies**
    
    - Reference values and records include `legal` and `acl` blocks.
        
    - Implication: you need at least a stub Legal Service (with tags like `opendes-public-usa`) and Entitlements Service (with groups like `data.default.owners@opendes.com`) or relax enforcement locally. Otherwise, ingestion will fail.
        
5. **Case & Encoding Rules are Strict**
    
    - Names must follow Title Case rules; Codes must be concatenated without spaces/punctuation.
        
    - Implication: if you add or extend reference values locally, you must follow the same casing/encoding rules, or your data won’t be interoperable with upstream OSDU.
        
6. **Load Order Matters**
    
    - Reference values → Schemas → Legal tags → Records.
        
    - Implication: your bootstrap sequence must mirror this order. If you try to ingest a Well record before its schema and reference values are loaded, it will fail.
        

### 🛠 Practical Next Steps for Your Local Setup

1. **Schema Service**
    
    - Already configured — ensure all schemas from `data-definitions` are discoverable.
        
2. **Legal Service**
    
    - Preload legal tags referenced in the test data (e.g. `opendes-public-usa`).
        
3. **Entitlements Service**
    
    - Either stub or configure groups like `data.default.owners@opendes.com`.
        
4. **Reference Data**
    
    - Load manifests from `ReferenceValues/Manifests` into Storage first.
        
5. **Domain Records**
    
    - Only after the above, ingest Wells, Wellbores, Seismic, etc.
        

### 🚦 Bottom Line

The README is telling you: _don’t treat these JSONs as isolated examples_. They are **interdependent**, and your environment must be configured to accept them “as‑is” — partitions, legal tags, ACLs, reference values, schemas — otherwise you’re not really testing OSDU compliance.

