| FieldName   | Description                        | OSDU Field             | Schema              | Mapping Class       | Reference Required | Decomposition Required |
|-------------|------------------------------------|------------------------|---------------------|---------------------|--------------------|-------------------------|
| WELLORIGIN  | Well origin code                   | wellOrigin             | Well                | Explicit            | No                 | No                      |
| WELLSTAT    | Well status                        | status                 | Well                | Explicit            | No                 | No                      |
| WELLTYPE    | Well type                          | wellType               | Well                | Explicit            | No                 | No                      |
| WELLCLASS   | Well class                         | wellClass              | Well                | Explicit            | No                 | No                      |
| WELLCONFIG  | Well configuration                 | configuration          | Well                | Explicit            | No                 | No                      |
| WELLPURP    | Well purpose                       | purpose                | Well                | Explicit            | No                 | No                      |
| WELLNAME    | Well name                          | name                   | Well                | Explicit            | No                 | No                      |
| WELLBORE    | Wellbore name                      | name                   | Wellbore            | Explicit            | No                 | No                      |
| WELLBOREID  | Wellbore ID                        | id                     | Wellbore            | Explicit            | No                 | No                      |
| TDMDDEPF    | Total depth MD (ft)                | depth.value (ft)       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| TDMDDEPM    | Total depth MD (m)                 | depth.value (m)        | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| TDTVDSSF    | Total depth TVDSS (ft)             | tvdss.value (ft)       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| TDTVDSSM    | Total depth TVDSS (m)              | tvdss.value (m)        | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STMDDATF    | Kickoff datum elevation (ft)       | datumElevation.value   | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STMDDATM    | Kickoff datum elevation (m)        | datumElevation.value   | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STRKDTMTY   | Kickoff datum type                 | datumType              | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STMDDEPF    | Kickoff MD (ft)                    | depth.value (ft)       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STMDDEPM    | Kickoff MD (m)                     | depth.value (m)        | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STTVDSSF    | Kickoff TVDSS (ft)                 | tvdss.value (ft)       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| STTVDSSM    | Kickoff TVDSS (m)                  | tvdss.value (m)        | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| GRNDELEV_F  | Ground elevation (ft)              | groundElevation.value  | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| GRNDELEV_M  | Ground elevation (m)               | groundElevation.value  | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| WATDEP_F    | Water depth (ft)                   | waterDepth.value       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| WATDEP_M    | Water depth (m)                    | waterDepth.value       | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| MXTDTEMPF   | Max hole temp (F)                  | temperature.value      | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| MXTDTEMPC   | Max hole temp (C)                  | temperature.value      | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| MNTDTEMPF   | Min hole temp (F)                  | temperature.value      | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| MNTDTEMPC   | Min hole temp (C)                  | temperature.value      | VerticalMeasurement | Reference Fragment  | No                 | Yes                     |
| PLATFORM    | Platform letter                    | facilityReference → name | Facility (custom) | Extension Needed    | Yes                | No                      |
| FACILITY    | Facility name                      | facilityReference → name | Facility (custom) | Extension Needed    | Yes                | No                      |
| FACTYPE     | Facility type                      | facilityReference → type | FacilityType       | Reference Fragment  | Yes                | No                      |
| FACSTATUS   | Facility status                    | facilityReference → status | Facility (custom) | Extension Needed    | Yes                | No                      |
| FIXMOBILE   | Drilling unit type                 | facilityReference → mobility | Facility (custom) | Extension Needed    | Yes                | No                      |
| FLUIDTYPES  | Anticipated development wellbore type | —                  | —                   | Extension Needed    | —                  | No                      |
| FLOWCLASS   | Original hydrocarbon flow class    | —                      | —                   | Extension Needed    | —                  | No                      |
| OTHERCLASS  | Other wellbore class               | —                      | —                   | Extension Needed    | —                  | No                      |
| WELLCONVEN  | Overall wellbore conventionality   | —                      | —                   | Extension Needed    | —                  | No                      |
| UNCWELTYP   | Unconventional wellbore type       | —                      | —                   | Extension Needed    | —                  | No                      |
| TEMPCLASS   | Temperature classification         | —                      | —                   | Extension Needed    | —                  | No                      |
| PRESSCLASS  | Pressure classification            | —                      | —                   | Extension Needed    | —                  | No                      |
| SDTRKTYPE   | Sidetrack type                     | —                      | —                   | Extension Needed    | —                  | No                      |
| PARENTROLE  | Parent wellbore relationship       | —                      | Wellbore            | Extension Needed    | Yes                | No                      |
| WELLINFO    | Information link                   | documentReference / informationLink | Document | Extension Needed | Yes                | No                      |
| COUNTRYCOD  | Regulatory jurisdiction            | countryCode            | Well                | Explicit            | No                 | No                      |
