# Chapter 9 — Local Auto Backup

---

## 1. What Is Local Auto Backup?

Local auto backup periodically copies your database file to a local directory on your device (e.g., iCloud Drive or a local folder), requiring no internet connection.

**vs. Cloud Backup:**

| Aspect | Local Auto Backup | Cloud Backup |
|--------|------------------|--------------|
| Internet required? | No | Yes |
| Storage location | Device local / iCloud Drive | Remote server |
| Trigger | Auto (on New/pagination/save) | Manual or auto-scheduled |
| Best for | Fast local protection | Cross-device sync |

---

## 2. Enabling Local Auto Backup

**Path:** Settings → Backup → Local Auto Backup

1. Turn on the **Local Auto Backup** toggle
2. Tap **Select Backup Directory** to choose the storage location:
   - iOS: recommended to choose a folder in **iCloud Drive** (auto-syncs to cloud)
   - Or a local device folder

---

## 3. When Backups Are Triggered

When enabled, backup triggers automatically on:

| Trigger | Description |
|---------|-------------|
| **Tap New (New Container)** | Auto-backs up the current project before starting a new one |
| **"Start New Page from Here"** | Auto-backs up after pagination |
| **Save in Internal Record editor** | Auto-backs up after editing a snapshot |

---

## 4. Managing Backup Files

**Path:** Settings → Backup → Local Auto Backup → Manage

The management page shows all backup files in the backup directory:
- View each file's name and date
- Manually delete old backups to free up space

---

## 5. Recommended Strategy

- Enable **both** local auto backup and cloud backup for dual protection
- Set the local backup directory inside iCloud Drive for local speed + cloud sync
- Periodically check the backup directory to confirm files are being created normally
