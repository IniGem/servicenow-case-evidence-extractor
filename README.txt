ServiceNow Case Evidence Extractor v2.5.2

Changes
- Restricts confirmed attachments to the active Activity stream or active Attachments panel.
- Requires exactly one filename and one file size in the smallest qualifying card container.
- Deduplicates attachments by normalized filename and size.
- Deduplicates cases by case number and prefers a single current-case entry.
- Includes related cases only when referenced in the current description or rendered Activity evidence.
- Forces OpenText KB links into OpenText resources regardless of author.
- Classifies ZIP, RAR, 7Z, GZ, TAR, TGZ, BZ2, and XZ as Archive before document fallback.
- Downloads remain user-triggered and use tickets/Account/Case with conflictAction=uniquify.

Test
1. Load unpacked and reload the case.
2. Keep the Activity attachment and Attachments panel visible.
3. Click Files & Links.
4. Confirm XML/HAR files outside those contexts are absent.
5. Confirm the current case appears once.
6. Confirm KB links are under OpenText resources.
7. Confirm RAR/ZIP files are Archive.
