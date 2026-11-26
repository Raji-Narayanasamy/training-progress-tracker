# Training Progress Tracker

A single-file web app to track learner progress across every training you run.

## Open it

Double-click `index.html` (any modern browser). No install, no server, no internet connection needed.

## What it does

- **Trainings**: name, category/client, trainer, dates, optional pass mark, and the list of modules.
- **Learners**: name, email, team/client, location.
- **Enrolments and progress**: enrol learners into trainings, mark modules complete, record an optional assessment score, and mark people as dropped.
- **Status** is calculated automatically:
  - Not started, In progress, Completed, Needs retake (below pass mark), Dropped.
- **At risk** flag: not completed and either past the training end date, or in progress with no activity for 14+ days.
- **Dashboard**: learners, completion rate, average score, and per-training breakdown.
- **Data**: export a progress CSV (for Excel or Power BI), import learners from CSV, export/import a JSON backup, load sample data, clear data.

## Data storage

Data is saved in the browser's local storage on the machine you use. It is not shared between people or devices. Use **Data → Export JSON backup** to move data or keep a copy. Importing a backup replaces existing data.

Because learner records can include personal data, keep the file and any exports within your normal data-handling rules.

## CSV import format

```
name,email,team,location
Jane Example,jane@example.com,Team Alpha,Site 1
```

Only `name` is required. Rows with a duplicate email are skipped.

## Files

- `index.html`: the whole application (HTML, CSS and JavaScript).
- `README.md`: this file.

## Known limits

- Single-user, browser-local storage. A shared, multi-user version would need a backend (for example, SharePoint lists, Dataverse, or a small database with login).
- Renaming or removing a module clears completion marks for that module.
- Sample data uses fictitious names only.
