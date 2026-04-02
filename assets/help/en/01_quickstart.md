# Chapter 1 — Quick Start

---

## 1. Opening the App for the First Time

On first launch, the app opens directly to the project list page.

### Creating Your First Project

1. Tap the **＋** button in the bottom-right corner, select **New Project**, then enter a **project name** (e.g., "March 2024 Imported Oak"), and tap **Create** to enter the main interface

> 💡 **Tip**: If projects already exist, simply tap a project card to open it. Long-press a card to reveal additional options.

---

## 2. The Main Interface at a Glance

```
┌─────────────────────────────────────────────────────────────┐
│ [+]  [Batch]  [⚙]     Project Name ▼      [💾]          │  ← Top Nav
├─────────────────────────────────────────────────────────────┤
│ ČSN 48 0009                              NO. 2            │
│                                                              │
│  Log ID: [________]         Notes: [________]              │
│                                                              │
│  Length(m): [__]  Diameter(cm): [__]     0.00 m³          │  ← Input Area
│                                                              │
│  Select Grade                                                │
│  [ABC] [A+] [A] [B] [C] [D]                               │  ← Grade Buttons
│                                                              │
│       [  +  Add & Continue  ]                               │
├─────────────────────────────────────────────────────────────┤
│ No │  Log ID  │ Grade │ Length(m) │ Diameter(cm) │ Volume │ Notes │  ← Header
├────┼──────────┼───────┼───────────┼──────────────┼────────┼───────┤
│ 1  │ 56748690 │   A   │   5.4    │     56      │1.13 m³│        │  ← List
└────┴──────────┴───────┴───────────┴──────────────┴────────┴───────┘
│                                                              │
│  [A: 1]    [Dual Tag]     Total: 1    Volume: 1.13 m³    │  ← Bottom Stats
└─────────────────────────────────────────────────────────────┘
```

**The interface has four zones:**

| Zone | Function | Description |
|------|----------|-------------|
| **Top Navigation** | Action buttons | New (refresh), Batch Profile, Settings, Project Switcher, Save |
| **Input Area** | Data entry | Log ID, Notes, Length, Diameter, Grade selector, Add button |
| **List Area** | Data display | Table of entered logs: ID, Grade, L/D, Volume |
| **Bottom Stats** | Real-time stats | Counts by grade, Dual Tag, Total count, Total volume |

---

## 3. Entering Your First Log

### Preparation

- **Log ID**: Enter manually, or leave blank for auto-increment (requires Quick Mode enabled in Settings)
- **Length** unit: meters (m), e.g. `3.5` = 3.5 m
- **Diameter** unit: centimeters (cm), e.g. `35` = 35 cm
- **Notes**: Optional field for special information

### Steps

1. **Enter Log ID** (optional)
   
   Type the log number/tag in the ID field

2. **Enter Length**
   
   Tap the length field and type `3.5`. Or enable **Quick Mode → Auto Decimal** in Settings — just type `35` and it becomes `3.5` automatically

3. **Enter Diameter**
   
   Tap the diameter field and type `35` (cm)

4. **Select Grade**
   
   Tap a grade button (**A**, **B**, **C**, etc.). Long-press a grade button to pick from saved favorites. Grades can be added or edited in **Settings → Grades & Deductions → Grade Pool**

5. **Tap Add**
   
   Tap **+ Add & Continue** — the entry saves to the list and bottom stats update instantly

> 🎯 **Try this**: Tap the "A: 1" badge in the bottom stats bar and see what happens! (Hint: it's a filter)

---

## 4. Essential Gestures

| Gesture | Effect | When to Use |
|---------|--------|-------------|
| **Swipe left on a row** | Shows action buttons (Insert / Delete / More) | When you need to delete or insert rows |
| **Long-press a grade button** | Select from saved favorite grades | Grades must exist in **Settings → Grades & Deductions → Grade Pool** first |
| **Tap a stats badge** | Filter the list (e.g., show Grade A only) | Quickly find all entries of a specific grade |
| **Long-press a stats badge** | Adjust statistics thresholds | Tweak short-log / thin-log standards |
| **Tap the Dual Tag button** | Toggle dual-tag mode | Used when one log is cut into two sections but not separated yet — it has two tags |

---

## 5. Input Error Correction

### Red Alert (Auto-correction)

If a row turns **red**, the input is likely invalid:

- ❌ Missing decimal point in length (e.g., `450` instead of `4.50`)
- ❌ Abnormal value entered (e.g., length over 20 m)

**Fix**: Tap the red row to edit it directly

---

## 6. Recommended Settings

### Beginner Mode (on by default)

**Path:** Settings → General → Beginner Mode

- ✅ On: Shows more guidance tips — great for first-time users
- ❌ Off: More compact interface — better for experienced users

### Quick Mode (strongly recommended)

**Path:** Settings → Input → Quick Mode

Enabling gives you three benefits:

| Feature | What it does | Example |
|---------|-------------|---------|
| Auto Decimal | Two digits auto-become a decimal | Type `35` → becomes `3.5` m |
| Auto Jump | Cursor moves to Diameter after Length | No manual field switching |
| Auto-increment Log ID | ID adds +1 on each entry | No manual ID entry needed |

> ⚠️ **Note**: Auto Decimal is not available in imperial unit mode

---

## 7. How is Volume Calculated?

The default formula is the cylinder equation:

```
V = π × (Diameter/200)² × Length
```

- Diameter in centimeters (cm)
- Length in meters (m)
- Result in cubic meters (m³)

> 📚 Need a different formula? See **Appendix A — Calculation Formulas** or switch in Settings

---

## 8. Saving and Exporting

### Auto Save

The app **auto-saves every entry** — no manual save needed. Even a sudden crash or power loss won't lose data.

When you finish the current batch and want to start a new one, tap the [↻] (refresh icon) **New** button in the **top-left**: after confirmation, the main list clears and **current list data is automatically saved as an internal record** (snapshot), viewable via **Save → Open Internal Records**. This cannot be undone — confirm the batch is complete first.

For an **extra manual backup**, tap **💾** → **Save to Internal Record**.

### Exporting Reports

After entry is done, tap **💾 Save/Export** at the top:

| Format | Purpose | How to Send |
|--------|---------|-------------|
| **PDF** | Official report with signature field | WeChat, email, print |
| **Excel** | Data analysis, editable | WeChat, email, computer |
| **Handover Share (.lmp)** | For colleagues to continue editing | See Chapter 7 |

---

## 9. What's Next?

Great job completing the basics! Recommended reading:

- **Chapter 2** → Project management, folders, search
- **Chapter 3** → List operations, dual tag, pagination
- **Chapter 12** → Hidden tips and shortcuts

Need help? Tap **?** in the top-right corner of the app, or go to **Settings → User Guide** for the full documentation.

---

**Happy measuring!** 🌲
