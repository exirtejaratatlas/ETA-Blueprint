# Journal Model

## Purpose

Defines the accounting journals used for recording financial transactions in ETA.

---

## Journal Types

- Sales Journal
- Purchase Journal
- Cash Journal
- Bank Journal
- General Journal
- Inventory Journal
- Tax Journal
- Payroll Journal
- Foreign Exchange Journal
- Adjustment Journal

---

## Journal Structure

Journal

- Journal ID
- Journal Code
- Journal Name
- Journal Type
- Company
- Currency
- Fiscal Period
- Status

---

## Journal Entry

Each Journal contains multiple Journal Entries.

Journal Entry

- Entry ID
- Entry Number
- Transaction Date
- Posting Date
- Reference
- Description
- Created By
- Approved By
- Approval Status

---

## Double Entry Support

Each Journal Entry contains:

- Debit Lines
- Credit Lines

Rules

- Total Debit = Total Credit
- Every Entry must balance
- No orphan transaction allowed

---

## Integration

Connected Modules

- Procurement
- CRM
- Sales
- Inventory
- Contracts
- Projects
- Finance
- Tax
- AI

---

## Future Extensions

- Auto Posting
- Recurring Journals
- AI Journal Suggestions
- Reversal Entries
- Multi Currency Posting
- Consolidation Journals