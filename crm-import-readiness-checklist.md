# CRM Import Readiness Checklist

Use this checklist before importing a CSV or Excel file into HubSpot, Salesforce, Pipedrive, Zoho, or another CRM.

## 1. Preserve the source

- Keep an untouched copy of the original export.
- Record the export date, source system, row count, and file format.
- Work on a duplicate, not the only copy.

## 2. Confirm the import key

Choose the field that identifies an existing record before removing duplicates. Examples include:

- CRM record ID
- Email address, when the business rules allow it
- An agreed combination such as account name plus domain

Do not guess the key. If the file does not contain one, put those rows into a review queue.

## 3. Inspect headers and values

Check for:

- Duplicate or blank headers
- Leading and trailing whitespace
- Inconsistent casing
- Mixed date formats
- Phone numbers stored in multiple formats
- ZIP or postal codes losing leading zeroes
- Boolean and status values that do not match the CRM's accepted values
- Formula errors or unexpected blank cells

## 4. Define duplicate behavior

Write down what happens when two rows match:

- Which row is retained?
- Which fields are merged, if any?
- Are discarded rows logged?
- Are ambiguous matches held for review?

A safe cleanup should be auditable rather than silently deleting uncertain records.

## 5. Validate against the target CRM

Before the full import, verify:

- Required fields are populated.
- Headers map to the intended CRM fields.
- Select fields use accepted values.
- Dates and numbers use the expected format.
- Record IDs remain text and are not reformatted by spreadsheet software.
- Relationships, owners, and tags have a defined mapping.

## 6. Run a small test

Use a redacted or fictional sample first. Import a small batch, inspect the result, and record any mapping changes before processing the full file.

## 7. Keep a delivery record

Save:

- Original row count
- Cleaned row count
- Rows held for review
- Duplicate rules used
- Field transformations
- Validation errors
- Final file name and date

## Need help?

For a reviewed one-file cleanup, request a fixed quote starting at **$75**:

https://rngbubba.github.io/mr-bubba-store/csv-cleanup-for-crm-import.html

Start with the file type, approximate row count, target CRM, and a fictional or redacted sample. Never send passwords, API keys, payment information, or confidential customer records through a public form.
