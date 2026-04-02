# Chapter 6 — Internal Records

---

## 1. What Are Internal Records?

An **internal record** is a **complete snapshot** of the current list at a specific moment in time.

It saves all log entries from that moment, allowing you to review historical data without interrupting ongoing entry.

> Analogy: an internal record is like taking a "photo" every time you finish loading a container — it preserves the complete measurement result.

---

## 2. Creating an Internal Record

**Method 1:** Save/Export menu → **Save to Internal Record**

**Method 2:** Use the **Start New Page from This Row** feature (see Chapter 3) — the split-off data is automatically saved as an internal record.

**Method 3:** When tapping **New (New Container)**, the app automatically saves the current list as an internal record, then clears it to start a fresh entry.

---

## 3. Viewing Internal Records

Tap **💾** at the top of the main interface → **Open Internal Records**

The viewer shows all internal records for this project, each containing:
- Record name and creation time
- Total pieces and total volume
- Tap to view the full log list

---

## 4. Internal Record Editor

Tap **Edit** on any record in the list to enter the editor:

### Basic Operations
- **View entries**: Shows all log details in the record
- **Edit data**: Modify Log ID, Grade, Length, Diameter, Notes directly
- **Add/delete rows**: Swipe left to delete; tap "+ Add" to insert
- **Sort**: Tap the **No.** column header to toggle ascending/descending order
- **Export**: Generate PDF / Excel for this record

### Dual Tag Grouping
- Long-press to select multiple rows → tap **Group** to mark them as one log (dual tag)
- Dual-tagged rows show a colored left border
- Swipe left on a dual-tagged row to ungroup

---

## 5. Verification (Data Validation)

**Purpose**: Cross-check against source documents (paper records, counterpart reports) entry by entry to find and correct discrepancies.

Enter the internal record editor → tap the **Verify** button and choose a mode:

### Mode A: List Verification
Best for fast batch checking — see many rows at once.

**How it works**:
- List shows all entries; scroll up/down to review
- Swipe left to mark: **Verified** (green) / **Questionable** (orange)
- Tap any field to edit directly
- Filter by: All / Unverified / Verified / Questionable

**Marker guide**:
| Marker | Meaning |
|--------|---------|
| No marker | Not yet verified |
| Green border | Verified — data is correct |
| Orange border | Questionable — needs further confirmation |

### Mode B: Entry-by-Entry (Card View)
Best for careful, focused inspection of individual logs.

**How it works**:
- Shows one log at a time in a large card format
- Swipe left/right to navigate between logs
- Tap fields to edit directly
- Bottom buttons for quick marking: ✓ Verified / ⚑ Questionable
- Shows live volume calculation for easy comparison with documents

**View toggle**:
- **Detail view**: Shows Log ID, Grade, Length, Diameter, Volume — all fields
- **Volume view**: Enlarged volume display for easy comparison with counterpart sheets

### After Verification
Tap **Done** — the system writes changes back to the internal record:
- Edited fields are updated
- Deleted rows are removed
- Added rows are inserted
- Verification status (verified/questionable) is preserved for future reference

---

## 6. Restoring an Internal Record to the Current List

### Purpose
Load a **copy** of a historical internal record into the current list, modify the differences, then **save as a new record**.

**Typical scenario**:
- Two containers have almost identical contents — only a few logs differ
- Restore the previous container's record, modify the differences, then save as the new container's record

### How
In the internal record editor, tap **Restore**:
1. The selected record's data is **copied** into the current list (the original record is not deleted)
2. Edit the entries that need changing in the current list
3. When done, tap **Save to Internal Record** again to save as a new snapshot

### ⚠️ Important Warning
**Restoring will overwrite the current main interface list!**

Before restoring, confirm that:
- The main list is **empty**, or
- The main list **has been saved as an internal record**

> 💡 Restoration is a **copy** operation — the original internal record is never deleted. You can restore the same record multiple times to create different versions.

---

## 7. Batch Export All Internal Records

On the project list page, tap a project card's **⋮** → **Export All Snapshots (Excel)**.

Generates a multi-sheet Excel file:
- **Sheet 0**: Summary of all records (name, date, piece count, volume)
- **Sheets 1–N**: Log details for each record

---

## 8. Importing Internal Records via JSON

Internal records can be imported from `.json` files (format: `oak_snapshot_export_v1`).

**How:** Save/Export menu → **Import Project File** → select the `.json` file.

> Before importing, save the current list as an internal record to prevent overwriting.
