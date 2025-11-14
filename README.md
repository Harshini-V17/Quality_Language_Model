Task 1: Ingestion, PHI Redaction & Provenance (Summary)

Goal

Build an end-to-end pipeline to ingest healthcare data, validate schema, redact PHI, generate a QLM-ready dataset, and produce provenance + integrity checks.

Inputs

1. source1_clinical_notes.jsonl

2. source2_lab_reports.csv

3. phi_rules.json

4. schema_definitions.json

5. metadata.json

Key Steps

1. Ingest JSONL & CSV using strict schemas

2. Apply regex-based PHI redaction

3. Normalize to a canonical QLM-ready structure

4. Generate row-level SHA-256 hashes

5. Generate batch-level hash for tamper detection

6. Create provenance JSON containing:

* batch_id

* source files

* PHI rules applied

* row count

* integrity hash

Outputs

1. Clean QLM-ready Delta dataset

2. Provenance JSON

3. Integrity verification script

Task 2: Data Lake Architecture (Summary)

Goal

Demonstrate a compliant Data Lake architecture with layered storage, governance, versioning, and auditing.

Layers Implemented

1. RAW – Untouched input files

2. BRONZE – Schema applied, minimally cleaned Delta tables

3. SILVER – Cleaned, redacted, standardized datasets

4. GOLD – QLM-ready analytics dataset

Governance Features

1. Delta Lake time travel and versioning

2. RBAC (least-privilege)

3. Audit events stored for operations

4. Provenance saved for each GOLD run

5. Encryption (TLS + cloud at-rest encryption)

Outputs

1. Complete Raw/Bronze/Silver/Gold lake structure

2. Audit logs

3. Access control matrix

4. Regulatory checklist

Technologies Used

1. PySpark

2. Databricks

3. JSONL, CSV, Parquet

4. Regex-based redaction
