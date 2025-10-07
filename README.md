# NSTA-OSDU-schema-checklist
This is my attempt to ingest components of the North Sea Transition Authority's (NSTA) Open Data into The Open Subsurface Data Universe (OSDU). Seems pretty fundamental, to me....

Data Mapping.

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
