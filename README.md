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

---

## 📋 Checklist Sections

Use the links below to jump to each section:

- [Part 1 — Well Identification & Lifecycle](#part-1--well-identification--lifecycle)
- [Part 2 — Intent, Status, and Classification](#part-2--intent-status-and-classification)
- [Part 3 — Location & Targeting](#part-3--location--targeting)
- [Part 4 — Licence & Operator](#part-4--licence--operator)
- [Part 5 — Reservoir, Deviation, Datum, Depths, Sidetrack, Elevations, Environment, Facility](#part-5--reservoir-deviation-datum-depths-sidetrack-elevations-environment-facility)
- [Part 6 — Fluids, Flow, Temperature, Pressure, Facility, Country](#part-6--fluids-flow-temperature-pressure-facility-country)

---

## ✅ Part 1 — Well Identification & Lifecycle

### Part 1 — Well Identification & Lifecycle

| NSTA Field | OSDU Field | OSDU Schema File | .json URL | .md URL | OSDU Schema |
|------------|------------|------------------|-----------|---------|-------------|
| WELLORIGIN | WellID | Wellbore.1.4.0.json | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y |
| ORIGINSTAT | OriginStatusID | Wellbore.1.4.0.json | [Link](same as above) | [Link](same as above) | Y |
| PARENTWELL | ParentWellID | Wellbore.1.4.0.json | [Link](same as above) | [Link](same as above) | Y |
| WELLREGNO | RegulatoryID | Well.1.0.0.json | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |
| SPUDDATE | SpudDate | Wellbore.1.4.0.json | [Link](same as WELLORIGIN) | [Link](same as WELLORIGIN) | Y |
| DATETDREAC | TDDate | Wellbore.1.4.0.json | [Link](same as WELLORIGIN) | [Link](same as WELLORIGIN) | Y |
| COMPLEDATE | CompletionDate | Wellbore.1.4.0.json | [Link](same as WELLORIGIN) | [Link](same as WELLORIGIN) | Y |
| RELEASEDAT | ReleaseDate | Wellbore.1.4.0.json | [Link](same as WELLORIGIN) | [Link](same as WELLORIGIN) | Y |

---

## ✅ Part 2 — Intent, Status, and Classification

### Part 2 — Intent, Status, and Classification

| NSTA Field   | OSDU Field         | OSDU Schema File         | .json URL                                                                 | .md URL                                                                 | OSDU Schema |
|--------------|--------------------|---------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------|-------------|
| ORIGINTENT   | OriginalIntentID   | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y *(needs ReferenceWellboreIntentType)* |
| CURRWELLIN   | CurrentIntentID    | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y *(needs ReferenceWellboreIntentType)* |
| DEVTYPE      | DevelopmentTypeID  | *ReferenceDevelopmentType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| COMPLESTAT   | CompletionStatusID | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| WELLOPSTAT   | WellOperationalStatusID | Well.1.0.0.json     | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |
| WELLSUFFIX   | WellSuffix         | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| WELLALIAS    | AliasName          | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| NAME         | Name               | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |

---

## ✅ Part 3 — Location & Targeting

### Part 3 — Location & Targeting

| NSTA Field   | OSDU Field           | OSDU Schema File         | .json URL                                                                 | .md URL                                                                 | OSDU Schema |
|--------------|----------------------|---------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------|-------------|
| SLOTNO       | SlotNumber           | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y |
| MULTILAT     | MultiLateralIndicator| Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| DESIGNATED   | DesignatedIndicator  | Well.1.0.0.json           | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |
| TARGETFLD    | FieldID              | Wellbore.1.4.0.json       | [Link](same as SLOTNO)                                                   | [Link](same as SLOTNO)                                                 | Y |
| PRIMARYTAR   | PrimaryTargetID      | Wellbore.1.4.0.json       | [Link](same as SLOTNO)                                                   | [Link](same as SLOTNO)                                                 | Y |
| PROSPECT     | ProspectID           | Wellbore.1.4.0.json       | [Link](same as SLOTNO)                                                   | [Link](same as SLOTNO)                                                 | Y |

---

## ✅ Part 4 — Licence & Operator

### Part 4 — Licence & Operator

| NSTA Field   | OSDU Field           | OSDU Schema File         | .json URL                                                                 | .md URL                                                                 | OSDU Schema |
|--------------|----------------------|---------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------|-------------|
| LICTYPE      | LicenceTypeID        | *ReferenceLicenceType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| LICNO        | LicenceID            | Well.1.0.0.json           | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y *(but Licence schema missing)* |
| TDLICNO      | LicenceAtTDID        | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y *(but Licence schema missing)* |
| SUBAREAOP    | SubAreaOperatorID    | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| SUBOPPREV    | PreviousSubAreaOperatorID | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| TDOPERATOR   | TDOperatorID         | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| TDOPPREV     | PreviousTDOperatorID | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |

---

## ✅ Part 5 — Reservoir, Deviation, Datum, Depths, Sidetrack, Elevations, Environment, Facility

### Part 5 — Reservoir, Deviation, Datum, Depths, Sidetrack, Elevations, Environment, Facility

| NSTA Field   | OSDU Field           | OSDU Schema File         | .json URL                                                                 | .md URL                                                                 | OSDU Schema |
|--------------|----------------------|---------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------|-------------|
| RESWOP       | ReservoirOperatorID  | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| RESWOPRES    | ReservoirID          | *Reservoir.1.0.0.json*    | N/A                                                                       | N/A                                                                    | N |
| RESWOPPREV   | PreviousReservoirOperatorID | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| RESDOP       | ReservoirDevelopmentOperatorID | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| RESDOPREAS   | DevelopmentReasonID  | *ReferenceDevelopmentReason.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| RESDOPPREV   | PreviousReservoirDevelopmentOperatorID | *ReferenceOperator.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| DEVIATTYP    | DeviationTypeID      | *ReferenceDeviationType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| DATUMTYPE    | VerticalMeasurementDatumID | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y *(needs ReferenceDatumType)* |
| DATELEV_F    | KickoffElevation_ft  | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| DATELEV_M    | KickoffElevation_m   | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDDEPDATTY   | TDMeasurementDatumID | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y *(needs ReferenceDatumType)* |
| TDDATDEP_F   | TDDepthDatum_ft      | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDDATDEP_M   | TDDepthDatum_m       | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDMDDEPF     | TDMeasuredDepth_ft   | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDMDDEPM     | TDMeasuredDepth_m    | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDTVDSSF     | TDTrueVerticalDepthSubsea_ft | Wellbore.1.4.0.json | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TDTVDSSM     | TDTrueVerticalDepthSubsea_m | Wellbore.1.4.0.json | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| TD_AGE       | TDGeologicalAge      | *ReferenceGeologicalAge.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| SDTRKTYPE    | SidetrackTypeID      | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y *(needs ReferenceSidetrackType)* |
| PARENTROLE   | ParentRoleID         | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y *(needs ReferenceParentRole)* |
| STMDDATF     | KickoffDatumElevation_ft | Wellbore.1.4.0.json   | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| STMDDATM     | KickoffDatumElevation_m | Wellbore.1.4.0.json    | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| STRKDTMTY    | KickoffDatumTypeID   | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y *(needs ReferenceDatumType)* |
| STMDDEPF     | KickoffMeasuredDepth_ft | Wellbore.1.4.0.json    | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| STMDDEPM     | KickoffMeasuredDepth_m | Wellbore.1.4.0.json     | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| STTVDSSF     | KickoffTVDSS_ft      | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| STTVDSSM     | KickoffTVDSS_m       | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| GRNDELEV_F   | GroundElevation_ft   | Well.1.0.0.json           | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |
| GRNDELEV_M   | GroundElevation_m    | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| WATDEP_F     | WaterDepth_ft        | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| WATDEP_M     | WaterDepth_m         | Well.1.0.0.json           | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |

---

## ✅ Part 6 — Fluids, Flow, Temperature, Pressure, Facility, Country

### Part 6 — Fluids, Flow, Temperature, Pressure, Facility, Country

| NSTA Field   | OSDU Field           | OSDU Schema File         | .json URL                                                                 | .md URL                                                                 | OSDU Schema |
|--------------|----------------------|---------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------|-------------|
| FLUIDTYPES   | FluidTypeID          | *ReferenceFluidType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| FLOWCLASS    | FlowClassificationID | *ReferenceFlowClass.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| OTHERCLASS   | OtherClassificationID| *ReferenceOtherClass.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| WELLCONVEN   | WellConventionalityID| *ReferenceWellConventionality.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| UNCWELTYP    | UnconventionalWellTypeID | *ReferenceUnconventionalWellType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| TEMPCLASS    | TemperatureClassID   | *ReferenceTemperatureClass.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| PRESSCLASS   | PressureClassID      | *ReferencePressureClass.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| MXTDTEMPF    | MaxTemperature_ft    | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y |
| MXTDTEMPC    | MaxTemperature_C     | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| MNTDTEMPF    | MinTemperature_ft    | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| MNTDTEMPC    | MinTemperature_C     | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| PLATFORM     | PlatformID           | *Platform.1.0.0.json*     | N/A                                                                       | N/A                                                                    | N |
| FACILITY     | FacilityID           | *Facility.1.0.0.json*     | N/A                                                                       | N/A                                                                    | N |
| FACTYPE      | FacilityTypeID       | *ReferenceFacilityType.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| FACSTATUS    | FacilityStatusID     | *ReferenceFacilityStatus.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| FIXMOBILE    | FacilityMobilityID   | *ReferenceFacilityMobility.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| WELLINFO     | WellInformationID    | *WellInformation.1.0.0.json* | N/A                                                                       | N/A                                                                    | N |
| WELLBRSTAT   | WellboreStatusID     | Wellbore.1.4.0.json       | [Link](same as above)                                                    | [Link](same as above)                                                  | Y |
| COUNTRYCOD   | CountryID            | Well.1.0.0.json           | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |

---

## 🧠 Notes

- Fields marked with `*italic schema names*` are **not yet available** in OSDU and may need to be scaffolded
- All links prefer the official OSDU repo at [community.opengroup.org](https://community.opengroup.org/osdu/data/data-definitions/)
- This checklist is designed to support ingestion, validation, and Swagger/OpenAPI flattening

### NOTES Supplimental — OSDU Required Components Missing from NSTA

| OSDU Field         | Purpose / Notes                                      | OSDU Schema File         | .json URL | .md URL | OSDU Schema |
|--------------------|------------------------------------------------------|---------------------------|-----------|---------|-------------|
| id                 | Unique record identifier (UUID)                      | All master/work schemas   | Required by OSDU core | N/A | Y |
| kind               | Schema type and version (e.g., `osdu:master-data:Well:1.0.0`) | All schemas | Required by OSDU core | N/A | Y |
| acl                | Access control list (who can read/write)             | All schemas               | Required by OSDU core | N/A | Y |
| legal              | Legal tags, data governance                          | All schemas               | Required by OSDU core | N/A | Y |
| data               | Container for actual business fields                 | All schemas               | Required by OSDU core | N/A | Y |
| meta               | Metadata about ingestion, versioning                | All schemas               | Required by OSDU core | N/A | Y |
| createTime         | Timestamp when record was created                    | All schemas               | N/A       | N/A     | Y |
| modifyTime         | Timestamp when record was last updated               | All schemas               | N/A       | N/A     | Y |
| version            | Version number of the record                         | All schemas               | N/A       | N/A     | Y |
| SurfaceLocation    | GeoJSON point or polygon for surface location        | Well.1.0.0.json           | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Well.1.0.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Well.1.0.0.md) | Y |
| BottomHoleLocation | GeoJSON point for bottom hole                        | Wellbore.1.4.0.json       | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/Generated/master-data/Wellbore.1.4.0.json) | [Link](https://community.opengroup.org/osdu/data/data-definitions/-/blob/master/E-R/master-data/Wellbore.1.1.0.md) | Y |
| SpatialExtent      | Bounding box or polygon for wells/fields             | *Field.1.0.0.json*        | N/A       | N/A     | N |
| ReferenceDatumType.1.0.0.json | Validates vertical measurement datum types | *ReferenceDatumType.1.0.0.json* | N/A | N/A | N |
| ReferenceSidetrackType.1.0.0.json | Validates sidetrack type values       | *ReferenceSidetrackType.1.0.0.json* | N/A | N/A | N |
| ReferenceLicenceType.1.0.0.json | Validates licence type values          | *ReferenceLicenceType.1.0.0.json* | N/A | N/A | N |
| ReferenceWellboreIntentType.1.0.0.json | Validates wellbore intent values | *ReferenceWellboreIntentType.1.0.0.json* | N/A | N/A | N |
---

## 📣 Contributions

Feel free to fork this repo, submit pull requests, or open issues to improve schema coverage or add missing reference definitions.

---

## 📜 License

This project is open source under the [MIT License](LICENSE).


