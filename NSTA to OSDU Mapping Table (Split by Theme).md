
### 🧠 Key Clarifications

- **OSDU schemas (Well, Wellbore, etc.) are abstract**: They define high-level concepts and relationships, not concrete field-level implementations. This abstraction is intentional to support extensibility across operators and regions, but it complicates direct mapping from structured datasets like NSTA.
    
- **ER diagrams on OSDU GitLab are conceptual**: They illustrate entity relationships and cardinality, but they don’t reflect the actual JSON schema structure or field-level constraints. So using them as a basis for field mapping can lead to misinterpretation or oversimplification.
    
- **NSTA fields are flat and concrete**: The NSTA open data schema is tabular, with well-defined field names and values. Mapping these to OSDU requires not just field alignment but also understanding of how OSDU expects data to be nested, referenced, or derived.
    

---

### 🌻 Implications for Mapping

- **Direct 1:1 field mapping is rare**: Most NSTA fields require transformation, enrichment, or contextual interpretation before they can be ingested into OSDU.
    
- **Intermediate models may be needed**: You might need a staging schema or transformation layer that bridges NSTA’s flat structure with OSDU’s abstract model.
    
- **Schema extensions or custom manifests**: In some cases, extending OSDU schemas or creating ingestion manifests tailored to NSTA data may be the most practical route.
    

---

### 📜 NSTA to OSDU Mapping Table (Split by Theme)

#### 🧭 Spatial & Depth Measurements

|FieldName|Description|OSDU Field|Schema|Mapping Class|Reference Required|Decomposition Required|
|---|---|---|---|---|---|---|
|TDMDDEPF|Total depth MD (ft)|[depth.value](https://depth.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|TDMDDEPM|Total depth MD (m)|[depth.value](https://depth.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|TDTVDSSF|Total depth TVDSS (ft)|[tvdss.value](https://tvdss.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|TDTVDSSM|Total depth TVDSS (m)|[tvdss.value](https://tvdss.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|STMDDATF|Kickoff datum elevation (ft)|[datumElevation.value](https://datumElevation.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|STMDDATM|Kickoff datum elevation (m)|[datumElevation.value](https://datumElevation.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|STRKDTMTY|Kickoff datum type|datumType|VerticalMeasurement|Reference Fragment|No|Yes|
|STMDDEPF|Kickoff MD (ft)|[depth.value](https://depth.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|STMDDEPM|Kickoff MD (m)|[depth.value](https://depth.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|STTVDSSF|Kickoff TVDSS (ft)|[tvdss.value](https://tvdss.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|STTVDSSM|Kickoff TVDSS (m)|[tvdss.value](https://tvdss.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|GRNDELEV_F|Ground elevation (ft)|[groundElevation.value](https://groundElevation.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|GRNDELEV_M|Ground elevation (m)|[groundElevation.value](https://groundElevation.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|WATDEP_F|Water depth (ft)|[waterDepth.value](https://waterDepth.value) (ft)|VerticalMeasurement|Reference Fragment|No|Yes|
|WATDEP_M|Water depth (m)|[waterDepth.value](https://waterDepth.value) (m)|VerticalMeasurement|Reference Fragment|No|Yes|
|MXTDTEMPF|Max hole temp (F)|[temperature.value](https://temperature.value) (F)|VerticalMeasurement|Reference Fragment|No|Yes|
|MXTDTEMPC|Max hole temp (C)|[temperature.value](https://temperature.value) (C)|VerticalMeasurement|Reference Fragment|No|Yes|
|MNTDTEMPF|Min hole temp (F)|[temperature.value](https://temperature.value) (F)|VerticalMeasurement|Reference Fragment|No|Yes|
|MNTDTEMPC|Min hole temp (C)|[temperature.value](https://temperature.value) (C)|VerticalMeasurement|Reference Fragment|No|Yes|

#### 🏗️ Facility & Infrastructure

|FieldName|Description|OSDU Field|Schema|Mapping Class|Reference Required|Decomposition Required|
|---|---|---|---|---|---|---|
|PLATFORM|Platform letter|facilityReference → name|Facility (custom)|Extension Needed|Yes|No|
|FACILITY|Facility name|facilityReference → name|Facility (custom)|Extension Needed|Yes|No|
|FACTYPE|Facility type|facilityReference → type|FacilityType|Reference Fragment|Yes|No|
|FACSTATUS|Facility status|facilityReference → status|Facility (custom)|Extension Needed|Yes|No|
|FIXMOBILE|Drilling unit type|facilityReference → mobility|Facility (custom)|Extension Needed|Yes|No|

#### 🏛️ Regulatory & Jurisdictional

|FieldName|Description|OSDU Field|Schema|Mapping Class|Reference Required|Decomposition Required|
|---|---|---|---|---|---|---|
|COUNTRYCOD|Regulatory jurisdiction|countryCode|Well|Explicit|No|No|

#### 🧪 Classification & Fluid Properties

|FieldName|Description|OSDU Field|Schema|Mapping Class|Reference Required|Decomposition Required|
|---|---|---|---|---|---|---|
|FLUIDTYPES|Anticipated development wellbore type|—|—|Extension Needed|—|No|
|FLOWCLASS|Original hydrocarbon flow class|—|—|Extension Needed|—|No|
|OTHERCLASS|Other wellbore class|—|—|Extension Needed|—|No|
|WELLCONVEN|Overall wellbore conventionality|—|—|Extension Needed|—|No|
|UNCWELTYP|Unconventional wellbore type|—|—|Extension Needed|—|No|
|TEMPCLASS|Temperature classification|—|—|Extension Needed|—|No|
|PRESSCLASS|Pressure classification|—|—|Extension Needed|—|No|

#### 🔗 Relationships & External References

|FieldName|Description|OSDU Field|Schema|Mapping Class|Reference Required|Decomposition Required|
|---|---|---|---|---|---|---|
|SDTRKTYPE|Sidetrack type|—|—|Extension Needed|—|No|
|PARENTROLE|Parent wellbore relationship|—|Wellbore|Extension Needed|Yes|No|
|WELLINFO|Information link|documentReference / informationLink|Document|Extension Needed|Yes|No|

Let me know when you're ready to export this as a `.md` file or scaffold the missing schema components next.
