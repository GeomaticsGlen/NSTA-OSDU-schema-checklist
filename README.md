# NSTA-OSDU-schema-checklist
This is my attempt to ingest components of the North Sea Transition Authority's (NSTA) Open Data into The Open Subsurface Data Universe (OSDU). Seems pretty fundamental, to me.... This is a first pass summary generated with my own guidance for reference - links will be provided to actual reality when available.

# 🛠️ OSDU Schema Checklist for NSTA Field Mapping

This project provides a complete mapping between **NSTA “New Field Names”** and their corresponding **OSDU schema fields**, including:

- ✅ Field equivalence
- ✅ Associated `.json` schema files
- ✅ `.md` documentation links
- ✅ Schema availability status
- ✅ Suggested schema names for missing components

---

## 📦 Repository Structure

- `README.md` — This file, containing the full checklist
- `schemas/` — Optional folder to store custom or scaffolded schemas
- `docs/` — Optional folder for extended documentation or examples

---## 🧠 Key Clarifications

- **OSDU schemas (Well, Wellbore, etc.) are abstract**  
  They define high-level concepts and relationships, not concrete field-level implementations. This abstraction supports extensibility across operators and regions, but complicates direct mapping from structured datasets like NSTA.

- **ER diagrams on OSDU GitLab are conceptual**  
  They illustrate entity relationships and cardinality, but don’t reflect the actual JSON schema structure or field-level constraints. Using them as a basis for field mapping can lead to misinterpretation or oversimplification.

- **NSTA fields are flat and concrete**  
  The NSTA open data schema is tabular, with well-defined field names and values. Mapping these to OSDU requires not just field alignment but also understanding of how OSDU expects data to be nested, referenced, or derived.

---

## 🧩 Implications for Mapping

- **Direct 1:1 field mapping is rare**  
  Most NSTA fields require transformation, enrichment, or contextual interpretation before they can be ingested into OSDU.

- **Intermediate models may be needed**  
  A staging schema or transformation layer might be necessary to bridge NSTA’s flat structure with OSDU’s abstract model.

- **Schema extensions or custom manifests**  
  In some cases, extending OSDU schemas or creating ingestion manifests tailored to NSTA data may be the most practical route.


  USING jonslo's Clone of the OSDU Gitlab Data Defintions.

#Controlled Fields

Well.1.4.0.json

| Field Name              | Reference Type                     | Reference JSON File                                                                 |
|-------------------------|------------------------------------|--------------------------------------------------------------------------------------|
| status                  | reference-data--WellStatus         | [WellStatus.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellStatus.1.0.0.json) |
| wellType                | reference-data--WellType           | [WellType.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellType.1.0.0.json) |
| purpose                 | reference-data--WellPurpose        | [WellPurpose.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellPurpose.1.0.0.json) |
| alias[].kind            | reference-data--AliasKind          | [AliasKind.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/AliasKind.1.0.0.json) |
| fieldReference          | master-data--Field                 | [Field.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Field.1.3.0.json) |
| facilityReference       | master-data--Facility              | [Facility.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Facility.1.3.0.json) |
| operatorReference       | master-data--Organization          | [Organization.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Organization.1.3.0.json) |
| countryReference        | master-data--GeoPoliticalArea      | [GeoPoliticalArea.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/GeoPoliticalArea.1.0.0.json) |


Wellbore.1.5.1.json
| Field Name         | Reference Type                     | Reference JSON File                                                                 |
|--------------------|------------------------------------|--------------------------------------------------------------------------------------|
| status             | reference-data--WellboreStatus     | [WellboreStatus.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellboreStatus.1.0.0.json) |
| wellType           | reference-data--WellboreType       | [WellboreType.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellboreType.1.0.0.json) |
| purpose            | reference-data--WellborePurpose    | [WellborePurpose.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/WellborePurpose.1.0.0.json) |
| alias[].kind       | reference-data--AliasKind          | [AliasKind.1.0.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/ReferenceValues/AliasKind.1.0.0.json) |
| facilityReference  | master-data--Facility              | [Facility.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Facility.1.3.0.json) |
| fieldReference     | master-data--Field                 | [Field.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Field.1.3.0.json) |
| operatorReference  | master-data--Organization          | [Organization.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Organization.1.3.0.json) |
| trajectoryReference| master-data--Trajectory            | [Trajectory.1.3.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Trajectory.1.3.0.json) |
| wellReference      | master-data--Well                  | [Well.1.4.0.json](https://github.com/jonslo/osdu-data-data-definitions/blob/master/SchemaRegistrationResources/shared-schemas/osdu/master-data/Well.1.4.0.json) |


➡️ [View Testing Outcomes and Refinements](testing.md)
This page documents the validation process, schema refinements, ingestion results, and next steps for aligning NSTA data with OSDU requirements.

## ✅ Current Status

_(Add your notes here)_

## 🔧 Refinement Tasks

_(Add your checklist or action items here)_


## 📣 Contributions

Feel free to fork this repo, submit pull requests, or open issues to improve schema coverage or add missing reference definitions.

---

## 📜 License

This project is open source under the [MIT License](LICENSE).


