# Chapter 2 — Project Management

## 1. Why Use Projects?

**Core purpose**: Completely separate data from different business operations — prevents mixed-up orders and makes management easier.

### Common Ways to Divide Projects

| Scenario | Approach | Example |
|----------|---------|---------|
| **Different containers** | One container = one project | Container A, Container B, Container C |
| **Different suppliers** | By supplier name | Zhang Wood, Li Forest Farm |
| **Different dates** | By date | March 15 Batch, March 20 Batch |
| **Different wood species** | By species | Oak Project, Pine Project, Beech Project |
| **Different customers** | By buyer | Customer A, Customer B |

> 💡 How you divide them is up to you. **The key rule: data within the same project is related; different projects are completely independent.**

### Each Project is Fully Independent

One project = one complete work unit, containing:

- **A dedicated log entry list** — belongs only to this project
- **Independent batch information** — container number, buyer/seller, wood species, etc.
- **Independent internal records (snapshots)** — all historical archives for this project
- **Independent statistics** — volume, grade distribution, amounts, etc.

> Switching projects = switching to a completely new data environment. No risk of data mixing.

---

## 2. Search

| Search Type | Description |
|-------------|-------------|
| **Keyword** | Search by project name or batch number (partial match works) |
| **Date Filter** | Filter by "Last Updated" date range |
| **Combined Search** | Keyword + date used together |

---

## 3. Folders

Use folders to organize when you have many projects:

| Action | How |
|--------|-----|
| **Create / Move** | Tap **⋮** on a project card → **Move to Folder** |
| **Collapse / Expand** | Tap the folder header |
| **Rename / Delete Folder** | Tap **⋮** next to the folder name → Rename or Delete (projects return to "Uncategorized") |

> A project can only belong to one folder at a time.

---

## 4. Project Card Actions

Tap **anywhere** on the card to enter the project.

Tap **⋮** on the right:

| Action | What it Does |
|--------|-------------|
| **Rename** | Change the project name |
| **Move to Folder** | Categorize into a folder |
| **Remove from Folder** | Return to "Uncategorized" |
| **Export All Snapshots (Excel)** | Export all historical snapshots as **one Excel file** (multiple sheets, one per snapshot) |
| **Archive / Unarchive** | Archived projects appear faded — useful for distinguishing active from completed |
| **Delete** | **Permanently deletes** the project and all its data (unrecoverable) |

---

## 5. Creating and Switching Projects

### Create a New Project
1. Tap **＋** in the bottom-right → **New Project**
2. Enter a **project name** (recommended: include date/location/container, e.g., `2024-03-15-ShanghaiPort-Oak`)
3. Confirm to enter the measurement interface

> Batch number, buyer/seller, etc. — after entering the project, tap **📋** in the top-left to fill these in.

### Switch Projects
- **Back to list**: Tap the **project number** at the top (e.g., 🌲 001)
- **Open another project**: Tap its card in the list

---

## 6. FAQ

| Question | Answer |
|----------|--------|
| Is there a project limit? | None — create as many as you want |
| Can I change the project number? | No — the system auto-assigns 001, 002… |
| Can data be lost? | Auto-save is on, but important data should be regularly exported as backup |
| Can I recover a deleted project? | **Not directly**, but if you made a **cloud backup** or **local backup** before deleting, you can re-import from that file |
| Do folders affect project data? | No — folders only organize the list display |
