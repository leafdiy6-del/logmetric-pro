# Chapter 10 — Settings

> Note: this chapter is numbered "Chapter 10" in the app's table of contents, but the file is numbered `11_settings`. The sections below follow the top-to-bottom order of the Settings drawer. Settings related to **moisture content MC, EMC, company name**, etc. are in the **Batch Profile** (project info pop-up), not in the Settings drawer — see "Batch Profile Integration" at the end of this chapter.

---

## 1. General Settings

### Theme

Toggle between **Dark** and **Light** mode.

### Language

Options: **中文**, **English**, **Slovenščina** (Slovenian).

### Bottom Safe Area Padding (Android only)

Adds extra padding below the input area when the system navigation bar or landscape orientation obscures it. Range: **0–100 dp**. Actual padding = `max(system safe area, this setting)`.

### Beginner Mode

When enabled, the interface shows additional guidance hints. Turn off once you're familiar with the app. The side panel also has a **User Guide** button that opens the built-in manual (chapters match `assets/help/`).

---

## 2. Input Settings

### Professional Keyboard (non-Android only)

On **iOS / macOS**, enable the built-in professional numeric keyboard to speed up entry (not available on Android).

### Key Press Sound

Play a click sound on number key taps.

### Confirm Before Adding

Show a confirmation dialog before saving, displaying current length, diameter, etc. for a second check — useful for preventing accidental taps.

### Save Success Sound

Play a short tone after a row is saved.

### Quick Mode

For fast, continuous field entry. Enabling reveals sub-options:

| Sub-option | Description |
|-----------|-------------|
| Auto Decimal Point | Numbers like `45` become `4.5` m automatically (same rules as main interface) |
| Auto Jump Length→Diameter | Cursor moves to Diameter after Length is entered |
| Save on Grade Tap | Tap a grade button to save directly — no need to tap the save button |
| Auto-increment Log ID | ID increments by +1 after each entry |
| Auto-save on Diameter | **When "Show Grade" is off**: Diameter can auto-save when conditions are met (see interface guide for details) |

> **Note:** Under **Imperial Input** (see "Length/Diameter Units" below), **Auto Decimal Point** and **Auto Jump Length→Diameter** are disabled.

---

## 3. Volume & Weight (the "Volume" section of Settings)

### Total Volume Overload Warning

When enabled, set a volume threshold (in **m³**). When the list's total volume exceeds this threshold, the top stats area gives a prominent warning (e.g., container capacity alert).

### Length / Diameter Input Units (important)

There is **no separate Metric/Imperial toggle** anymore. The current logic:

- When **Enable Custom Volume Formula** is on and the selected formula is a **board foot (BF) type**, length is entered in **feet (ft)** and diameter in **inches (in)**.  
  BF-type formulas include: `Doyle`, `Roy`, `Scribner Decimal C`, `International 1/4"` and their **lookup table variants** (`Scribner [BF]` table, `Intl 1/4" [BF]` table), etc. (matching `isImperialFormula` in the code).
- All other cases use **metric**: length in **meters (m)**, diameter in **centimeters (cm)**.

Length/diameter deductions display in inches in imperial mode, but are stored internally in centimeters.

### Enable Custom Volume Formula

Off: uses the default cylinder formula **V = π × (d/200)² × L** (d in cm, L in m).

On: choose from a dropdown grouped by category (e.g., **Basic**, **A Type**, **CZ/SK**, **A. Nilson**, **Other**, **B Type Lookup**, **HU**, etc.):

- **Europe / Universal**: Huber (EN 1309-2), Czech ČSN 48 0009, Slovak实测表 `Lookup Table-igor`, etc.
- **North American BF**: Doyle, Roy, Scribner Dec.C, International 1/4" (and their table variants)
- **Other Math Formulas**: Hoppus, JAS, NF B53-020, Ontario, MARN, Local Java, D²L coefficient, Firewood, etc.
- **CZ/SK Series**: ČSN/STN, Smrek, Buk, Dub, etc.
- **B Type SQLite Lookup**: GOST 2708-75, ISO 4480-83, Scribner / Intl table versions, etc.
- **Hungarian HU Series**, etc.

Switching the formula **recalculates** all entries' volumes.

### Volume Decimal Places

Choose **0–3** decimal places for display and storage rounding.

### Board Foot Rounding (BF formulas only)

Shown only when the current formula is **Doyle / Roy / International 1/4"** (or their `intl14Table` variants):

- **Doyle / Roy**: None / Round down / Round up / Round
- **International 1/4"**: includes **USFS** options related to official rules (options may differ from Doyle/Roy)

> Rounding for other BF formulas (e.g., Scribner) follows the formula specification in Appendix A. **Non-BF formulas are unaffected by this setting.**

### Show Weight in Stats Bar / Weight Unit

Requires a wood species set in **Batch Profile** and entries with volume. Shows an **estimated total weight** in the stats bar.  
Weight unit: **auto** (kg < 1000, t ≥ 1000), fixed **kg**, or fixed **t**.  
Moisture content **MC (%)** is set in Batch Profile and used in weight conversion — see below.

---

## 4. Grades & Deductions (the "Grades" section of Settings)

### Show Grade

When off, grade buttons can be hidden from the main interface (Quick Mode's "Auto-save on Diameter" behavior changes accordingly).

### Number of Grade Buttons on Main Interface

**2–6** slots; grades not on buttons are still accessible via the in-row selector.

### Grade Pool Management

Expand to **add / delete / reorder** grades (up to **15** total). If you delete a grade that's already in use, you'll be prompted to reassign those entries to an unknown grade (dialog specifics vary).

### Long-press Grade Button to Rename

Long-press a grade button on the main interface to rename it directly.

### Compute Diameter (Derived Diameter)

When on, diameter can be derived from other measurement rules. Choose a **rounding method**: Round up / Round down / Mixed (see dropdown for details).

### Length / Diameter Deductions

For defects, bark removal, etc.: **Length Deduction**, **Diameter Deduction** (units follow current metric/imperial input: cm or in).

**Show deducted values in list**: On → the list shows the already-deducted dimensions. Off → the interface shows the original input values, with deductions applied only in **volume calculation**.

---

## 5. Pricing

### Enable Pricing

When on, unit prices and amounts can be used in exports.

### Currency

Supports **EUR €**, **USD $**, **CNY ¥**, and others (see dropdown for full list).

### Pricing Mode

| Mode | Description |
|------|-------------|
| Fixed Unit Price | Same unit price for all entries (per m³, BF, etc.) |
| By Grade | Set a different unit price per grade in the Grade Pool |
| By Species + Grade | Most granular — enter prices per species/grade combination on the pricing page (supports buy price/sell price, buyer/seller, etc. — see interface for details) |

### Tax Rate

Set a VAT percentage; reports calculate tax amounts and totals automatically.

### Show Prices in PDF / Excel

Separately controls whether **PDF** and **Excel** exports include price columns (only meaningful when "Enable Pricing" is on).

> **Company name in exports**: the "Show in PDF" toggle for "My Company" is in the **Batch Profile**, not in this pricing section (see "Batch Profile Integration" below). Export behavior for Excel follows the same setting.

---

## 6. Export Options (the "Export" section of Settings)

- **Show directional markers in PDF/Excel**: include directional-type markers in exports.
- **Show dual tags in PDF/Excel**: include dual-tag columns in exports (consistent with list group display).

For the full export workflow, see **Chapter 5 — Saving & Exporting**.

---

## 7. Backup (inside Settings)

- **Local Auto Backup**: toggle, directory selection, change folder, manage backup files, etc.
- **Cloud Backup**: toggle, connection status, manage cloud backups, etc.

Full details: **Chapter 8 — Cloud Backup** and **Chapter 9 — Local Auto Backup**.

---

## Batch Profile Integration (Moisture Content · EMC · Weight · Company Info)

The following are in **Main Interface → Batch Profile / Project Info**, **not** in the Settings drawer:

### Moisture Content MC (%)

Located near **Wood Species, Density** — tap to edit. Used for **weight estimation** and moisture-related alerts.

### MC Shortcut Presets & Environmental EMC Estimation

Presets: Kiln-dried, Air-dried ~12%, Construction lumber, Fiber saturation point 30%, Green lumber, etc. (see interface).

**Environmental EMC estimation**: enter **Temperature (°C)** and **Relative Humidity (%)** to estimate the **equilibrium moisture content EMC** using the Hailwood-Horrobin model — can be **applied to MC**.

> **EMC is an equilibrium target, not something added to current MC.** For example, if current MC is 30% and environmental EMC is 12%, the wood will trend toward **~12% over time**, not 42%.

### Estimated Total Weight

Shown in the Batch Profile area when a wood species is selected and total volume exists (in m³), working with the "Stats Bar Weight" setting.

### Company Name & PDF

Edit buyer/seller company information; the **"Show in PDF"** toggle for company names uses the corresponding switch in Batch Profile (same logic for Excel export — see actual export for final behavior).

---

## Verification Checklist

1. Open Settings and compare each section top-to-bottom with this guide.
2. Switch between **Huber** and **Doyle**, confirming that input units switch between **m/cm** and **ft/in**.
3. Open Batch Profile and confirm that MC, environmental estimation, and company display toggles are in the locations described above.
