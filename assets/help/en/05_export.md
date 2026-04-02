# Chapter 5 — Saving & Exporting

## 1. Export Overview

**Purpose**: Export entered log data as standardized reports (PDF/Excel) for archiving, sharing, and reconciliation.

**Supported formats**:
- **PDF**: Standard measurement report, ideal for printing and emailing
- **Excel**: Editable spreadsheet data, good for further analysis
- **JSON**: Full project backup (complete data)
- **ZIP**: PDF + Excel + JSON bundled together

---

## 2. Save/Export Menu

Tap **💾 Save/Export** (top-right of main interface) to open the action menu:

### Top Section — Data Management

| Option | What it Does |
|--------|-------------|
| **Save to Internal Record** | Saves current entries as a snapshot (internal record) for later viewing or recovery |
| **Open Internal Records** | View all historical snapshots for this project; can restore or export them |
| **Import Project File** | Import data into the current project from a JSON backup |

### Bottom Section — Export & Share

| Option | What it Does |
|--------|-------------|
| **Handover Share** | Creates a `.lmp` file — the recipient opens it in LogMetric Pro and data **auto-imports** for continued entry |
| **Generate PDF** | Exports the standard measurement report (company info, log details, summary stats) |
| **Export Excel** | Exports an editable `.xlsx` with detail data and summaries |
| **ZIP Bundle Export** | Packages PDF + Excel + JSON in one download |

> After export, use the system share sheet to send via WeChat, email, etc., or save locally.

---

## 3. PDF Export Contents

The generated PDF report contains the following sections:

### Header
- Title: **PACKING LOG LIST / SHIPMENT**
- Solid bottom border line

### Company Info (optional)
- Your company (left): name, address, phone, email, tax ID, bank account
- Buyer/Seller (right): same fields

### Project Info Table
- Date
- Container number
- Description
- Location
- Measured by
- Batch notes

### Log Detail Table
| Column | Description |
|--------|-------------|
| No. | Row number |
| Log ID | Log identifier |
| Grade | Grade label (e.g., F, A, B) |
| Length | Meters (m) or feet (ft) |
| Diameter | Centimeters (cm) or inches (in) |
| Volume | Cubic meters (m³) or board feet (BF) |
| Amount | If pricing is enabled |
| Notes | Per-row notes |

**Styling**:
- **Zebra striping**: alternating gray/white rows
- **Group markers**: Dual-tagged rows have a blue bold left border with bold text
- **Markers**: Flagged length/diameter/grade values show a ↑ suffix

### Price Summary (if pricing enabled)
- By grade: quantity, volume, unit price, amount
- Totals: total pieces, total volume, average unit price, subtotal
- Tax amount (if tax rate set)
- Total with tax

### Summary Stats
- Total pieces, total volume
- Grade distribution (e.g., F:15 pcs A:20 pcs)
- Small size stats (e.g., <4m:3 pcs <30cm:5 pcs)

### Footer
- LogMetric Pro | Export date

---

## 4. Excel Export Contents

The Excel file contains:

### Header Rows (first 3–4 rows)
- Row 1: Date + Company name (if company display is set)
- Row 2: Container number + Seller (if present)
- Row 3: Description + Location + Measured by (if present)
- Row 4: Batch notes (if present)

### Data Table
Same column structure as PDF, supports:
- Marker symbols (↑)
- Group background color (light blue) and borders

### Summary Section
- Total pieces, total volume
- Grade statistics table
- Small size stats (<4m, <2.5m, <30cm)
- Price statistics (if enabled)

### Multi-Snapshot Export
Multi-sheet structure:
- Sheet 0 "Summary": overview of all snapshots — dates, containers, piece counts, volumes
- Sheets 1–N: full data for each snapshot (same format as above)

---

## 5. Handover Share (.lmp File)

### Purpose
Package the current project data into a `.lmp` file to send to a colleague. The recipient **taps the file and it auto-imports** into their LogMetric Pro — seamless handover.

### Typical Scenarios

| Scenario | Description |
|----------|-------------|
| **Shift handover** | Worker A measures halfway, then sends `.lmp` to Worker B who continues entry |
| **Phone died/faulted** | Quick data transfer to another phone to keep working |
| **Team collaboration** | Field staff sends to office staff who continue editing or export reports |

### How to Use
1. Tap **Handover Share** → choose how to send (WeChat, email, AirDrop, etc.)
2. Recipient taps the `.lmp` file → chooses **Open in LogMetric Pro**
3. Confirms import → data appears in the project list ready for editing

### Characteristics
- **Price fields are auto-cleared** (protects commercial secrets)
- Includes: log list, batch info, internal records, current settings
- Recipient can immediately continue entry — no restart needed

---

## 6. ZIP Bundle Export

**Purpose**: Get all formats for a project in one download.

**Contains**:
- JSON backup (complete data)
- PDF report (print-ready)
- Excel spreadsheet (edit-ready)

---

## 7. Export Options

**Path:** Settings → Export Options

| Option | Description |
|--------|-------------|
| **Show markers in PDF/Excel** | Flagged length/diameter/grade values display the ↑ symbol |
| **Show groups in PDF/Excel** | Dual-tagged rows highlighted with blue borders and background |
| **Show company info in PDF** | Displays your company and buyer/seller info at the top of the report |
| **Show prices in PDF/Excel** | Exports amount columns and summaries when pricing is enabled |

### Pricing Settings
**Path:** Settings → Pricing

**Pricing modes**:
- **Fixed unit price**: same price for all grades
- **By grade**: different unit price per grade
- **By species + grade**: most granular — different price per species/grade combination

**Tax rate**: Set a VAT rate; reports automatically calculate tax and totals.

---

## 8. After Export

Three options for handling exported files:

| Option | Description |
|--------|-------------|
| **Share** | Send via system share sheet — WeChat, email, WhatsApp, etc. |
| **Save to Downloads** | Save directly to the device's Downloads folder |
| **Choose location** | Custom filename and save path via system dialog |

> iOS primarily uses the share sheet; Android can save locally first then share.

---

## 9. Filename Rules

Files are auto-named with:
- **PDF**: `OakLog_Container#_Date_Time.pdf`
- **Excel**: `Date_Batch#_Container#.xlsx`
- **JSON backup**: `LogMetricPro_Backup_Container/Batch_Date_Time.json`
- **Handover file**: `LogMetricPro_Handover_Container/Date_Time.lmp`
- **ZIP**: `OakLog_export_Date_Time.zip`

---

## 10. FAQ

| Question | Answer |
|---------|--------|
| Can't open Excel? | Use Microsoft Excel or a compatible app (e.g., WPS) to open `.xlsx` files |
| Chinese characters garbled? | PDFs use the Noto Sans SC font for proper Chinese rendering |
| Can exported Excel formulas calculate? | Volume values are stored as numbers, usable in formulas directly |
| Don't want to share price info? | Use **Handover Share** — prices are auto-cleared |
| Export a single internal record? | Open **Internal Records** → select a record → export PDF/Excel/JSON |
