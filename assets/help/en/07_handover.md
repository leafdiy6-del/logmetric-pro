# Chapter 7 — Handover Share

---

## 1. What Is Handover Share?

Handover Share lets you quickly share **the project data you're currently editing** with a colleague or the next shift. They can pick up exactly where you left off and continue editing seamlessly.

**vs. Exporting Reports:**

| Feature | Purpose | Recipient |
|---------|---------|-----------|
| **Handover Share** (.lmp) | Transfer unfinished work | Opens in LogMetric Pro to continue editing |
| **Export Report** (PDF/Excel) | Generate a final report for archiving/reconciliation | Opens in Office/WPS to view |

---

## 2. Sending a Handover File

### Steps

1. **Open the Save/Export menu**
   
   Tap **💾 Save/Export** at the top of the main interface

2. **Choose Handover Share**
   
   Select **Handover Share** from the menu

3. **Choose how to send**
   
   The system generates a `.lmp` file and opens the share sheet:
   - **WeChat** → send to a colleague or work group
   - **Email** → send to their inbox
   - **AirDrop** → fast transfer between Apple devices
   - **Other apps** → QQ, DingTalk, WeCom, etc.

### Handover File Characteristics

- **Format**: `.lmp` (LogMetric Pro proprietary format)
- **Filename**: `LogMetricPro_Handover_Container/Date.lmp`
- **Prices**: **automatically cleared** (protects commercial confidentiality)
- **Includes**: all log data, batch info, internal records, current settings

---

## 3. Receiving and Opening a Handover File

### Flow

When you receive a `.lmp` file:

1. **Tap the file**
   
   Find the `.lmp` in WeChat, email, or another app and tap it

2. **Choose how to open**
   
   Select **Open in LogMetric Pro** from the menu

3. **Confirm import**
   
   The app shows a confirmation dialog:
   ```
   Import Handover File
   Import this handover file? It will appear in your project list after import.
   [Cancel]  [Import]
   ```

4. **Start editing**
   
   After import, the project appears in your project list — tap it to **continue editing where the handover left off**

> 💡 **Note**: Importing creates a new project; it does not overwrite your existing projects.

---

## 4. Typical Scenarios

### Scenario A: Multi-person接力 on the Same Project

```
Shift A worker:
1. Enters some log data
2. Before end of shift, taps "Handover Share" to send to Shift B worker
3. Shift B worker receives it and continues entry for the remaining logs
```

### Scenario B: Cross-Device Work

```
Field staff:
1. Enters data on iPad
2. Sends via AirDrop or WeChat to the office computer
3. Office staff continues on the Mac version
```

### Scenario C: Supervisor Review Loop

```
Operator:
1. Completes entry, sends handover to supervisor
2. Supervisor reviews and revises, then sends handover back
3. Operator gets the finalized, approved data
```

---

## 5. Notes

### Price Information

The `.lmp` file **automatically clears all price data**, including:
- Fixed unit prices
- Per-grade unit prices
- Price-related settings

This protects the sender's commercial confidentiality. The recipient can set their own prices after import.

### Data Security

- Handover files are transmitted via third-party apps (WeChat/email) — be mindful of information security
- For sensitive data, consider using encrypted email or corporate network transfer
- Cloud backup (Chapter 8) is a more secure transfer option

### Version Compatibility

- `.lmp` files require the same or a newer version of LogMetric Pro
- If you get a format incompatibility error, both parties should update to the latest version

---

## 6. Comparison with Traditional Export

| Comparison | Handover Share (.lmp) | Export Project File (.json) |
|------------|---------------------|---------------------------|
| **Primary use** | Quick work handover | Full backup or long-term archive |
| **Price info** | Auto-cleared | Preserved |
| **File size** | Smaller | Larger (includes snapshots) |
| **Ease of use** | One-tap share | Multi-step operation |
| **Best for** | Daily shift handover | Full backup & migration |

---

## 7. FAQ

**Q: Can I send the same handover file multiple times?**
A: Yes. Each send captures the current data snapshot. You can send to multiple people.

**Q: What if they don't have LogMetric Pro installed?**
A: They need to install the app first. If they only need to view data, send a PDF or Excel report instead.

**Q: Do handover files expire?**
A: No. `.lmp` files can be stored long-term, but import promptly to avoid version issues.

**Q: Can I send to multiple people at once?**
A: Yes — select multiple recipients in the share sheet.
