# Chapter 3 — Main Interface Operations

## 1. Entering Logs

### Basic Steps

1. Fill in **Log ID** (optional), **Length** (m), **Diameter** (cm) in the bottom input area
2. Tap a **grade button** at the top (e.g., F) → the current row saves to the list automatically
3. The list shows the calculated volume for that row in real time

### Log ID

- Auto-increments by default (previous row +1)
- Can be manually changed; if changed, the system asks whether to auto-correct subsequent rows

### Number of Grade Buttons

Settings → Input → Visible Grade Count (2–6). Reduce the number of visible buttons to match how many grades you actually use.

---

## 2. List Operations

### Swipe Left

Swipe left on any row to reveal action buttons:

| Button | Action |
|--------|--------|
| Actions (···) | Insert row above / Insert row below / Renumber / Start new page from here |
| Delete | Permanently remove this row |

### Long-press Row Number

Long-press the **sequence number** at the start of a row to get the same menu as the swipe Actions menu.

### Inline Editing

**Log ID, Length, Diameter, and Notes** in the list can be tapped and edited inline — changes save in real time.

Grade can be changed via a dropdown menu.

---

## 3. Dual Tag

**Path:** Bottom toolbar → Dual Tag (long-press to enter)

Dual Tag mode marks multiple log rows as belonging to the same single log, preventing double-counting of pieces.

- Dual-tagged rows show a **colored vertical bar** on the left
- Swipe left on a dual-tagged row → tap **Remove Dual Tag** to unlink them

---

## 4. Start New Page from This Row

### Purpose
When a container is full (e.g., max 21 m³) but you've already entered 23 m³, the **excess** needs to go into the next container. This feature moves the specified row and everything below it to a **new entry page**, eliminating duplicate entry.

### How
1. **Swipe left** on any row, tap **Actions (···)**
2. In the bottom menu, select **Start New Page from Here**

### Effect
- The row **and everything above it** stays on the current list
- Everything **below the row** moves to a new entry page
- Auto-saved as an internal record; accessible anytime

> 💡 Common use: quickly split overflow into the next container without manually copying entries one by one.

---

## 5. Volume Overload Warning

After setting a total volume warning threshold (Settings → Volume → Total Volume Overload Warning), when the list's total volume exceeds the threshold:
- The top stats area turns **orange/red** as a warning
- Helps you catch overloading in time
