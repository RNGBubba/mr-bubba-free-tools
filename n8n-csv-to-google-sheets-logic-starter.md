# n8n CSV-to-Google-Sheets Logic Starter

A credential-free starter for a common workflow: receive rows, normalize values, identify a stable record key, and decide whether each row should be updated or appended in Google Sheets.

This is a **logic reference**, not a drop-in connection to anyone's Google account. It does not contain credentials, contact data, or a live API connection.

## Suggested flow

```text
CSV attachment or webhook
        ↓
Parse CSV / convert to items
        ↓
Normalize headers, whitespace, dates, and IDs
        ↓
Choose a stable key (for example: order_id)
        ↓
Search the destination sheet
   ↙ match              ↘ no match
Update the row          Append a row
        ↓                    ↓
             Log exceptions and counts
```

## Rules to decide before building

1. Which input starts the workflow?
2. Which field is the stable record key?
3. Which fields may be overwritten on an update?
4. What happens when the key is missing or duplicated?
5. How should malformed rows be reported?
6. What sample input and expected output define acceptance?

## Safe sample rows

```csv
record_id,customer_name,total,observed_at
A-001,Example One,12.50,2026-09-15
A-002,Example Two,8.00,2026-09-15
```

Use fictional or redacted rows while scoping. Keep Google, n8n, and other credentials in the buyer's own accounts and connect them only through an agreed secure method after scope is confirmed.

## Need implementation?

Mr Bubba Services offers a bounded implementation starting at **$150**:

https://rngbubba.github.io/mr-bubba-store/n8n-csv-google-sheets.html

The paid scope covers one agreed workflow, testing notes, and handoff documentation. Extra systems and ongoing support are quoted separately.
