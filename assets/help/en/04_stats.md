# Chapter 4 — Statistics & Filtering

---

## 1. Bottom Stats Bar

The main interface's bottom bar shows real-time summary data for the current list:

- **Total pieces** and **total volume** (m³ or BF)
- **By grade**: e.g. `F: 12` = Grade F has 12 pieces entered
- **Short log count**: e.g. `< 4m: 3` = 3 pieces under 4 m in length
- **Thin log count**: e.g. `< 30cm: 5` = 5 pieces under 30 cm in diameter
- **Weight estimate** (requires a wood species set in Batch Profile and weight display enabled)

---

## 2. Quick Filter by Tapping Stats Badges

**Tap** any stats badge at the bottom (e.g., tap `F: 12`):

- All matching rows in the list are **highlighted**
- Non-matching rows **dim out**
- Tap the same badge again or tap empty space to clear the filter

> **Use case:** Instantly locate entries of a specific grade or size — ideal for verification and review.

---

## 3. Custom Statistics Thresholds

**Action:** Long-press a short-log or thin-log stats badge

A dialog appears to adjust:
- **Short log threshold L1** (default 4 m)
- **Short log threshold L2** (default 2.5 m)
- **Thin log threshold D** (default 30 cm)

Changes take effect immediately — useful for adapting to different delivery standards.

---

## 4. Weight Estimate

**Prerequisites:**
1. Set the **wood species** in Batch Profile (affects wood density)
2. Settings → General → enable **Show Weight in Stats Bar**

Weight formula:

```
Weight (kg) = Total Volume (m³) × Wood Density (kg/m³) × Moisture Content Correction Factor
```

Default moisture content is 12% (standard air-dried wood); can be changed in Batch Profile.

**Weight units:**
- `auto`: shows kg below 1000 kg, t at 1000 kg and above
- Or fix to `kg` or `t` in Settings

---

## 5. Grade Distribution at a Glance

Stats by grade help you:
- Quickly confirm whether piece counts by grade match expectations
- Compare proportions across grades
- Do a final check before exporting reports
