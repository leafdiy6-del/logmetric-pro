# Chapter 11 — Hidden Tips & Operations

---

## 1. Real-time Error Detection (Red Alert)

If a row in the list appears in **red**, that entry has an invalid input.

**Common causes:**
- Missing decimal point in length (e.g., entered `450` instead of `4.50`)
- Entered an abnormal 3-digit length

**Purpose:** Provide immediate feedback at the moment of entry, ensuring 100% accuracy in measurement reports.

---

## 2. Custom Grade Names

**How:** Long-press a grade button in Settings or on the main interface.

**Purpose:** Flexibly rename grades to match customer requirements or trade standards (e.g., change the default "F" to "AB").

Grade pool management in Settings lets you add, delete, and reorder grades.

---

## 3. Real-time Bottom Summary

The bottom of the screen shows automatic statistics in real time:

- **By grade**: e.g., `F: 2` means 2 logs of Grade F have been entered
- **By length**: e.g., `< 4m: 1` means 1 log under 4 meters has been entered

---

## 4. Quick Locate & Highlight

**How:** **Tap** a summary stat at the bottom (e.g., tap `F: 2`).

**What it does:** All matching logs in the list are selected and highlighted. Even with hundreds of entries, you can instantly find what you're looking for — great for verification.

---

## 5. Flexible Statistics Threshold Adjustment

**How:** **Long-press** a length stat item (e.g., long-press `< 4m`).

**What it does:** Freely set the filter boundary. Whether you need to filter under 4 m or 4.5 m, long-press to customize instantly.

---

## 6. Long-press Row Number to Insert + Auto-renumber

**How:** Long-press a row's **sequence number**, then choose **Insert Row Above** from the menu.

Combined with "Auto-renumber": after entering a new Log ID in the new row, the system automatically updates all subsequent row numbers in sequence.

**Use case:** If you realize you missed logging one log, you can insert a row at that position and renumber without editing each row manually.

---

## 7. Dual Tag — In Depth

### What is Dual Tag?

Dual Tag marks **multiple rows as belonging to the same single log**. For example, if a long log is sawn into two pieces and measured separately, without marking it would be counted as two logs — dual tagging tells the system to treat them as one.

### Steps

1. **Enter Dual Tag mode**: Long-press the **Dual Tag** button in the bottom toolbar
2. **Select rows to mark**: Tap the rows you want to group (a colored vertical bar appears on the selected rows' left edge)
3. **Confirm**: Long-press the Dual Tag button again or tap elsewhere to exit the mode

### Dual Tag Appearance

- A **colored vertical bar** on the left side of tagged rows
- **Piece count = 1** in statistics; volume accumulates all segments
- Exports show a dual-tag indicator

### Removing a Dual Tag

Swipe left on a dual-tagged row → tap **Remove Dual Tag**.

### Typical Use Cases

| Situation | How to Handle |
|-----------|---------------|
| An 8 m log cut into two 4 m + 4 m pieces | Enter both pieces, then mark as dual tag — counts as 1 piece |
| Irregular log head measured separately | Mark body + head as dual tag |
| Oversized log measured in multiple sections | Mark all sections as the same dual tag group |

---

## 8. Start New Page from This Row

**How:** Long-press a row's **sequence number**, then select **Start New Page from Here** from the menu.

The system saves all content below that row to an internal record. The row and everything above it stays in the current list; entry continues from that row.

**Use case:** When you realize the current container has exceeded its target volume — instead of redoing everything, save the overflow to an internal record and keep working on the current list.
