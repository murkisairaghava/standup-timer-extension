# ⏱️ Standby Timer

A lightweight **Microsoft Edge / Google Chrome side-panel extension** for keeping standup meetings focused.

Standby Timer supports both **person-based** and **story-based** standups, tracks blockers and speaking time, and lets users save or export reports locally.

> No login. No backend. No database. No cloud synchronization.

---

## ✨ Features

### 👥 Person mode

Person mode starts with an empty engineer list. Add your team members under Manage engineers. The list is stored locally in your browser for future standups.
- Select the engineer currently speaking
- Start, pause, reset, and save speaking time
- Record multiple updates for the same engineer
- View cumulative speaking time
- Add or remove engineers dynamically
- Record the task or story being discussed

### 📋 Story mode

- Starts with an empty story queue
- Add stories/tasks before or during standup
- Assign an engineer to each item
- Time individual story updates
- Remove stories when no longer required

### 🚩 Blockers

Mark an update as a blocker while timing it. The blocker indicator is included in saved reports and exports.

### 📊 Reports

- View the active standup session
- Save completed standups locally
- Reopen previously saved reports
- Delete old reports to reclaim local browser storage
- Export active or saved reports as CSV
- Export active or saved reports as Excel `.xlsx`

---

## 🔐 Privacy and storage

Standby Timer does **not** use authentication or a backend service.

The following data is stored locally by the browser:

- Engineer list
- Story/task list
- Saved standup reports
- Timing history
- Blocker indicators

Data is not automatically shared between users or laptops.

> Export important reports before removing the extension, because uninstalling the extension may remove its locally stored data.

---

# 📦 Installation

No Node.js, npm, VS Code, or development environment is required to install the compiled extension.

## 1. Download Standby Timer

Go to the repository's **Releases** section and download:

```text
standby-timer-extension.zip
```

## 2. Extract the ZIP

Extract the ZIP to a permanent folder.

Example on Windows:

```text
C:\Users\<username>\StandbyTimer
```

The extracted folder should contain:

```text
StandbyTimer/
├── assets/
├── index.html
├── manifest.json
└── service-worker.js
```

The folder containing `manifest.json` is the folder that must be loaded into the browser.

---

# 🌐 Install in Microsoft Edge

1. Open Microsoft Edge.
2. Enter the following in the address bar:

   ```text
   edge://extensions
   ```

3. Enable **Developer mode**.
4. Select **Load unpacked**.
5. Select the extracted Standby Timer folder containing `manifest.json`.
6. Open the Edge **Extensions** menu.
7. Pin **Standby Timer** to the toolbar.
8. Select the Standby Timer icon to open the side panel.

---

# 🌐 Install in Google Chrome

1. Open Google Chrome.
2. Enter:

   ```text
   chrome://extensions
   ```

3. Enable **Developer mode**.
4. Select **Load unpacked**.
5. Select the extracted Standby Timer folder containing `manifest.json`.
6. Pin Standby Timer from the Extensions menu.
7. Select the Standby Timer icon to open the side panel.

---

# 🚀 Daily use

After installation, no terminal or npm command is required.

```text
Open Edge / Chrome
        ↓
Click Standby Timer
        ↓
Choose Person or Story mode
        ↓
Run standup
```

---

# 👥 Person mode

1. Select **Person**.
2. Select the engineer currently speaking.
3. Optionally enter the task/story being discussed.
4. Select **Start**.
5. Use **Pause** if necessary.
6. Select **Save** when the update is complete.
7. Select the next engineer.

An engineer can speak multiple times. Each saved segment is recorded separately while Standby Timer also keeps cumulative timing for that engineer during the active session.

---

# 📋 Story mode

Story mode intentionally begins with an empty queue so each squad can add only the items relevant to the current standup.

1. Select **Story**.
2. Enter a story/task name.
3. Select the responsible engineer.
4. Select **Add**.
5. Repeat for other stories.
6. Select a story from the queue.
7. Start and save the timing.

---

# 📁 Exporting reports

After at least one timing is saved, the **CSV** and **Excel** actions become available.

Generated filenames follow this format:

```text
standby-timer-YYYY-MM-DD_HH-MM-SS.csv
standby-timer-YYYY-MM-DD_HH-MM-SS.xlsx
```

The Excel export is a real `.xlsx` workbook.

---

# 💾 Saved reports

Select **Save report** to retain the completed standup inside the browser.

Saved reports can later be:

- Viewed
- Downloaded as CSV
- Downloaded as Excel
- Deleted individually
- Deleted together using **Delete all**

---

# 🔄 Updating Standby Timer

When a newer release is available:

1. Download the latest `standby-timer-extension.zip`.
2. Extract it.
3. Replace the files in the existing Standby Timer extension folder.
4. Open:

   ```text
   edge://extensions
   ```

   or:

   ```text
   chrome://extensions
   ```

5. Find **Standby Timer**.
6. Select **Reload**.
7. Close and reopen the extension side panel.

> Avoid removing the extension unless a clean reinstall is intended. Export important reports before a clean reinstall.

---

# 🛠️ Troubleshooting

## Load unpacked is unavailable

Make sure **Developer mode** is enabled.

If Developer mode is blocked by organizational browser policy, the extension will need to be distributed through the organization's approved extension-management process.

## `manifest.json` cannot be found

Make sure the selected directory directly contains:

```text
manifest.json
```

Do not select the ZIP itself. Extract the ZIP first.

## The extension side panel is blank

1. Open `edge://extensions` or `chrome://extensions`.
2. Find Standby Timer.
3. Select **Reload**.
4. Close and reopen the side panel.

If the problem remains, extract a fresh copy of the latest release and load the extracted directory again.

## Reports are missing on another laptop

This is expected. Standby Timer stores data locally and does not synchronize reports between devices.

## CSV / Excel buttons are disabled

Save at least one timing first. Export actions remain disabled while no timings exist in the active session.

---

# 📁 Repository contents

This distribution repository contains only the compiled browser extension and documentation:

```text
assets/
index.html
manifest.json
service-worker.js
README.md
LICENSE
```

Users do **not** need the React source code, `node_modules`, Vite, npm, or Node.js to install or run the extension.

---

# 🧭 Browser support

| Browser | Status |
|---|---|
| Microsoft Edge | ✅ Supported |
| Google Chrome | ✅ Supported |
| Mozilla Firefox | Not currently tested |
| Safari | Not currently supported |

---

# 🤝 Feedback

Feedback and contributions are welcome, especially around:

- Standup facilitation workflows
- Person-based versus story-based updates
- Accessibility
- Side-panel usability
- Report formats
- Multi-squad adoption

Use GitHub Issues to report problems or suggest enhancements.

---

# 📄 License

See `LICENSE` for licensing information.
