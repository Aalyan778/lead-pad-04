# LeadPad

LeadPad is a single-file lead tracker. You paste leads one at a time, it checks each one against everything you have recorded before, numbers the new ones, and sets duplicates aside with the reason. It runs entirely in your browser: no install, no account, no internet needed.

## Getting started

1. Open `LeadPad.html` in a browser (Chrome or Edge recommended).
2. Paste a lead into the box at the top (Ctrl+V), or type and press Ctrl+Enter.
3. Watch the message line under the box: green means a new lead was added, red means it was a duplicate.
4. At the end of the day, save your files (Excel, .txt or Word) and click **New day**.

## How duplicate checking works

A lead is checked against all leads you have recorded before, including previous days. These items count as a match:

- Phone number
- Email address
- Any link (website, Google Maps, Facebook, Instagram)
- Business name + address (from lines like `Name: ...` and `Address: ...`)
- Same company website or email domain (can be switched off with the **Same domain = duplicate** checkbox; free mail like Gmail and platforms like Facebook are not treated as company domains)

What happens depends on how much matches:

- **Everything matches:** the lead goes to the **Duplicates** tab with the reason.
- **Only some items match:** the repeated items are removed and only the new information is kept.
- **Same business as an existing lead:** the new details are added to that lead instead of creating a new one.
- **Nothing matches:** the lead is added as the next numbered lead.

Leads with no phone, email or link are still saved, but a warning tells you they could not be checked.

## The header

| Item | What it shows |
|---|---|
| **N / Goal leads** | New leads today against your daily goal (default 400) |
| **Today: ...** | New, duplicate and partial counts for today |
| **📧 N emails · M leads with email** | Total distinct email addresses in your New leads, and how many leads have at least one email |
| **🎯 N / Email goal email goal** | Email progress against your email goal (default 400) |
| **Goal** and **Email goal** boxes | Change either goal; both are remembered |
| **Record: N keys** | Size of the permanent record used for duplicate checking |

When you reach the leads goal, a celebration popup and sound play.

## Buttons

- **⚡ Auto-paste:** when on, copying a lead elsewhere and switching back to LeadPad adds it automatically. Your browser must allow clipboard access for this page.
- **🔊 Sound / volume:** a different sound for new leads, duplicates and reaching the goal.
- **↶ Undo (Ctrl+Z):** undoes the last action, up to 60 steps.
- **Copy all:** copies all new leads, numbered, to the clipboard.
- **Stats:** a table of the last 7 days (new, duplicates, partial).
- **Auto-backup / Backup now / Restore backup:** see Backups below.
- **Check CSV file:** runs every row of a CSV through the duplicate check.
- **Save Excel:** one row per business, with all of its emails in one cell. Sheets: *Leads with email*, *No email*, *About this file*.
- **Save .txt / Save Word:** numbered lists of your new leads.
- **Ignore list:** emails, websites or phones to skip when checking duplicates. They are still included in your saved files. The default list contains `zooreach@zooreach.org` and `zooreach.org`.
- **Export record / Import record:** save or load the permanent record as a CSV.
- **Open .txt:** load a previously saved .txt list back in.
- **New day:** clears today's New and Duplicates lists. The permanent record is kept.

Other features: a search box that looks through today's leads and the old record, editable lead text, a ✕ button to delete a lead, **Recheck duplicates** (moves duplicates back to New if they no longer match), and **Save duplicates .txt** on the Duplicates tab.

## Backups (please read)

Everything is stored in your browser's own storage on this computer. Clearing site data, using a different browser or profile, or a private window means the data will not be there.

- A backup file is saved automatically every 100 new leads (if **Auto-backup** is ticked), or any time you click **Backup now**.
- Backup files end in `.json.gz` (or `.json`). Keep a copy on a USB stick or cloud drive.
- **Restore backup** replaces the current list and record with the backup.
- Backups include leads, duplicates, stats, the leads goal, the ignore list and the record. They do **not** include the email goal, so set it again after restoring.

## Notes

- Leads are plain text. Lines like `Name: ...`, `Address: ...` and `Phone: ...` give the best results, but any text with a phone, email or link works.
- Saved Excel files contain one row per business, so a business with several emails is one row with all its addresses in the *Email Addresses* column.
