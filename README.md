# DigiTally

> Track what's owed. Know when it's due. Invoice — or receipt — it when it's time.

A simple, persistent bill tracker and ledger with built-in invoicing and receipts. Add entries as you go, group by week or month, see the total at a glance — and when it's time to get paid (or confirm you were), generate a formal PDF in one click. Works for freelancers, video editors, shopkeepers, or anyone tracking money between two people — whether it's owed *to* them or *by* them, and in whatever currency they actually use.

## Features

- Multiple clients / projects, with **inline rename** — renaming a client carries all its entries, notes, details, currency, and share link with it
- Add entries with description and amount, in the client's own currency
- **Edit any entry** — fix a typo or wrong amount in place, no delete-and-retype
  - The original transaction date stays locked; an "edited on" stamp is recorded instead, so nothing can be changed silently
  - The edit marker shows in the app, on shared views, and on the PDF
- Per-client **private notes** — jot down anything for yourself; these stay private and never appear on a PDF
- **Invoice & Receipt PDF** — generate a formal, branded document from any client's entries in one click
  - **Invoice / Receipt toggle** — Invoice pulls unpaid entries ("Total Due"); Receipt pulls paid entries ("Total Paid", marked **Paid in Full**)
  - **Pick your line items** — choose exactly which entries go on the document with checkboxes; the total updates live
  - **Bill To — structured client details** — Name, Phone/Number, Email, Country, Address, saved per client and prefilled next time; built cleanly onto the document (your private notes are never used here)
  - Auto numbering — invoices (INV-0001…) and receipts (RCT-0001…) on separate counters, synced across devices
  - Your business name, contact, and payment details — saved once, prefilled forever
  - Due date (invoices) / paid-on date (receipts)
  - Multi-page support for long entry lists
- Group by All, This Week, or This Month
- **Mark all paid / unpaid** — one tap to settle everything in view; tap again to undo
- Mark entries as paid individually
- Running total — owed vs paid
- Copy full summary to clipboard
- Export data as CSV (pick which clients; includes each entry's currency)
- Share a read-only client view via link
- **Share Overview** — share a date-range summary link across selected clients
- **Delete paid entries** (two-step confirm); deleting a client also asks for confirmation
- **Per-client currency — any world currency** — choose from ~160 currencies with a searchable picker. Each client displays in its own currency, auto-detected from the entries you typed in it, so a client in one country and a client in another each show in their own money — no carry-over. A one-time **Choose Currency** prompt sets your default for new clients, and the header pill shows the active currency clearly (e.g. `$ USD`, `৳ BDT`). The picker on the header lets you view any client in another currency to see the converted equivalent.
- Each entry is stored in the currency it was typed in; totals convert per entry, so even mixed-currency clients add up correctly
- Real exchange rates powered by a live rates API (updated hourly, no key needed); the four built-in defaults (USD, INR, PKR, BDT) work offline
- Sticky brand bar on scroll, dark and light mode
- **Data never disappears** — synced to the cloud via Firebase, accessible from any device, any browser

## Account & Sync

Sign up with your email. Your clients, entries, edit history, invoice and receipt counters, per-client details, per-client currency, and business info are saved to your account permanently — accessible from any device, any browser. Nothing disappears unless you delete it yourself. Access is locked down per user with Firestore security rules; shared links are read-only.

## No backend to manage

100% client-side HTML. Firebase handles auth and sync. PDF invoices and receipts are generated entirely in your browser via jsPDF — nothing is uploaded anywhere. Currency rates are fetched once and cached for an hour.

## Use cases

- Freelancer tracking per-project work and invoicing clients directly
- Video editor logging deliverables per client and billing the unpaid ones
- Shopkeeper keeping a running tab and issuing paid receipts
- Anyone, anywhere, tracking money they're owed — or money they owe — in their own currency, and keeping a clean record of both

## Run it

Open [`https://itsultium.github.io/Digi-Tally/`](https://itsultium.github.io/Digi-Tally/) in any browser. No build step needed — it's a single HTML file.

## Built by

[Bruder Motion](https://github.com/itsultium)

## License

Copyright © 2026. This project is licensed under the GPL-3.0 License — see the [LICENSE](LICENSE) file for details.
