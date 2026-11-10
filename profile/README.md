# elmnt

elmnt reads a person's blood report, works out which supplements they actually need, and has a registered doctor check and sign the plan before anything reaches the customer.

## What we are building

- A customer books a home blood test with our lab partner Thyrocare, or uploads a report they already have.
- The report is read, the numbers are checked by plain code, and a medical rules engine drafts a supplement plan.
- A registered doctor reviews the draft, can change it, and signs it. Nothing reaches a customer unsigned.
- The customer gets the plan on screen and as a PDF. The supplements are packed and shipped, and the customer retests every few months.

## What it is made of

- A website and customer portal for customers.
- A dashboard for doctors, operations and inventory staff.
- A backend API, and a background processor that reads each report.
- A phone app, later.

All of it is written in TypeScript in one repository: `elmnt1/elmnt-monorepo` (private). The plan, decisions and build checklists are in its `docs/` folder.

## Rules we never break

- The AI reads numbers off a report. It never prescribes.
- A registered doctor signs every plan, after at least 90 seconds of review.
- Three consents are recorded before any health data is processed.
- Health data is protected by the database itself, and personal data is kept out of logs and error reports.

## Status

We are in the foundation stage. The project structure, tooling, database and sign-in are being built and tested. No customer-facing feature is live yet.
