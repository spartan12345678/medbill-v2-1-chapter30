MEDBILL v2.1 - CHAPTER 30 HSN REFERENCE DEVELOPMENT BUILD

This is an offline-first browser/PWA prototype for pharmacy billing and inventory. It is not approved for commercial use or GST compliance.

DATA PRESERVATION
- The application continues to use IndexedDB database medbill-local-v1, version 2.
- Existing batches, invoices and shop settings are not intentionally deleted or migrated by this release.
- Export a fresh backup before deploying or testing.
- Do not clear Chrome site data/storage.
- Never upload transaction backups, customer data, GST certificates, passwords or API keys to GitHub.

CHAPTER 30 CATALOGUE
- hsn-chapter30.json contains 228 tariff entries extracted from the user-supplied Chapter 30 PDF.
- Search is available by HSN/tariff item, heading and extracted description.
- Entries are unverified classification references. The catalogue does not assign HSN codes to stock items and does not populate GST rates.
- Source descriptions are preserved as extracted and may contain OCR or table-extraction noise. Check the source PDF page before relying on an entry.
- The supplied PDF is a customs tariff reference, not a GST-rate database. Customs duty figures must not be treated as GST rates.
- Scope is Chapter 30 only. It is not a complete HSN catalogue for all pharmacy goods.

DEPLOYMENT AND TESTING
1. Keep the current V2 repository/deployment unchanged.
2. Upload all files in this folder to a separate development repository or branch, including hsn-chapter30.json.
3. Serve over HTTPS and open the development URL in Chrome on Android.
4. Use dummy data only for testing.
5. Test Billing, Inventory, Invoices, Shop setup, Backup and the new HSN reference search.
6. Test offline by opening the app once online, then switching to airplane mode and searching Chapter 30 entries.
7. Confirm the HSN reference screen does not change any stock item or GST rate automatically.

KNOWN LIMITATIONS
- No live HSN or GST database integration.
- No automatic classification or GST-rate assignment.
- Source extraction may contain OCR/table parsing errors; verify against the PDF and current official tariff.
- No e-invoice, e-way bill, GST return filing, credit-note workflow, sales returns, supplier purchase module, user roles, encryption, cloud sync or multi-device sync.
- Backup JSON is not encrypted. Store it securely.
- Browser/PWA local storage is not a substitute for a managed, backed-up production database.
- Verify applicable GST provisions, invoice particulars, drug licence details, pharmacy recordkeeping and data-protection obligations with qualified professionals before commercial use.
