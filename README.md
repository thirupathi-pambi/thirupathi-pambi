# Thirupathi Pambi

I work in healthcare IT. Most of what's here is small Python tools built around problems that come up between clinical systems: messages that don't parse, patient data that doesn't add up, and reports nobody fully trusts.

Every project uses made-up data, runs on plain Python with nothing to install, and has unit tests. In each README I've written down the decisions I made and what I'd add next.

## Interoperability

- **[hl7v2-adt-message-validator](https://github.com/thirupathi-pambi/hl7v2-adt-message-validator)**: Parses HL7 v2 ADT messages and flags missing segments and fields. It also handles the MSH-1 separator quirk that trips up a lot of hand-written parsers.
- **[fhir-r4-patient-observation-etl](https://github.com/thirupathi-pambi/fhir-r4-patient-observation-etl)**: Takes a FHIR R4 Bundle, links each Observation back to its Patient, and writes one flat CSV row per result.

## Data quality

- **[ehr-data-quality-automation](https://github.com/thirupathi-pambi/ehr-data-quality-automation)**: Checks patient and encounter files for duplicate IDs, bad dates and orphaned encounters, and writes an issue list someone can work through.
- **[clinical-trial-data-management](https://github.com/thirupathi-pambi/clinical-trial-data-management)**: Tracks study visit completion and raises queries for incomplete adverse event records. Includes a SQL version of the visit metrics.

## Testing and go-live

- **[ehr-upgrade-uat-framework](https://github.com/thirupathi-pambi/ehr-upgrade-uat-framework)**: A UAT tracker for an EHR upgrade. It reports pass rates by module and open defects, and gives a release gate that won't say "ready" while anything is failed, blocked or not run.

## Operations and risk

- **[healthcare-operations-analytics](https://github.com/thirupathi-pambi/healthcare-operations-analytics)**: Clinic no-show and cancellation rates, calculated in both Python and SQL, plus a static HTML dashboard.
- **[healthcare-security-risk-register](https://github.com/thirupathi-pambi/healthcare-security-risk-register)**: Scores security findings on likelihood × impact and lists the high risks that are still open.
- **[healthcare-it-asset-risk-prioritization](https://github.com/thirupathi-pambi/healthcare-it-asset-risk-prioritization)**: Ranks clinic devices for replacement based on condition, Windows 10 status and age.

## Tools I use

Python, SQL, HL7 v2, FHIR R4, CSV/JSON pipelines, unittest
