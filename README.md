# Veil: Personal Data Redactor

A browser-only tool that finds personal data in pasted text, highlights it, and gives you a masked version to share safely.

**Privacy:** everything runs in your browser. Nothing is uploaded or stored.

## What it detects

Emails, Indian mobile numbers, Aadhaar, PAN, PIN codes and dates of birth, plus common Indian names (optional).

## Features

- Highlights each match with its type
- Redacted output with three mask styles: `[PHONE]`, partial (`XXXX XXXX 1234`) and pseudonyms (`[EMAIL_1]`)
- Switch each type on or off, and click a highlight to un-mark a false positive
- Summary table, Copy and Export buttons, `.txt` / `.csv` import
- Dark mode and a one-click Judge test

## Avoiding false positives

- **Aadhaar** must pass the Verhoeff checksum, so random 12-digit invoice numbers are ignored.
- **Phone numbers** match many formats (`+91 98765 43210`, `98765-43210`, `9876543210`) but never inside a longer number.
- **PIN codes and dates of birth** are only flagged next to words like "PIN" or "DOB".
- Overlapping matches are resolved by priority, so the output is never corrupted.

## Limitations

Detection is pattern-based, so review the result before sharing.

## Run locally

Open `index.html` in a browser. No install needed.
