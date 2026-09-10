# File System Access

## Quick Overview

| Name               | Definition                                                         | Example                                  |
| ------------------ | ------------------------------------------------------------------ | ---------------------------------------- |
| File System Access | Allows an AI agent or program to interact with files and folders.  | Read a CSV file and create a report.     |
| Read               | Gets data from an existing file.                                   | Read customer data from `customers.csv`. |
| Write              | Creates a new file or saves changes to a file.                     | Save a generated report as `report.txt`. |
| File Management    | Organizes files and folders by moving, renaming, or deleting them. | Move old logs into an `archive` folder.  |

## 1. Read Files

**Definition:** Reading lets an AI agent open a file and use its contents as input.

**Example:**

```text
AI Agent → Read sales.csv → Analyze the sales data
```

**Instructions:**

* Use reading when the agent needs information stored in a file.
* Check that the file exists before reading it.
* Only allow access to files the agent is authorized to use.
* Avoid exposing sensitive or private data unnecessarily.

## 2. Write Files

**Definition:** Writing lets an AI agent create a new file or save changes to an existing file.

**Example:**

```text
AI Agent → Generate report → Save as report.txt
```

**Instructions:**

* Use writing to save reports, results, or logs.
* Check the file path before writing.
* Avoid overwriting important files without permission.
* Use appropriate file formats for the data being saved.

## 3. Manage Files and Folders

**Definition:** File management lets an AI agent organize files by creating, moving, renaming, or deleting them.

**Example:**

```text
AI Agent → Find old logs → Move them to /archive
```

**Instructions:**

* Give the agent access only to required folders.
* Be careful with delete and move operations because they can cause data loss.
* Use clear folder and file names to keep data organized.
* Keep backups when file operations could affect important data.

## 4. File System Security

**Definition:** File system security prevents an AI agent from accessing or changing files it should not control.

**Example:**

```text
Allowed:  /project/reports/
Blocked:  /system/
```

**Instructions:**

* Follow the principle of least privilege: give only the permissions the agent needs.
* Restrict access to sensitive system and user files.
* Validate file paths to prevent unintended access.
* Log important file operations so they can be reviewed.

## 5. End-to-End Workflow Example

**Definition:** An AI agent can combine file reading, processing, writing, and file management to complete a task automatically.

**Example:**

```text
1. New sales.csv arrives
        ↓
2. AI Agent reads the file
        ↓
3. Agent analyzes the sales data
        ↓
4. Agent generates a summary report
        ↓
5. Agent saves report as sales_report.txt
        ↓
6. Agent moves sales.csv to /archive
        ↓
7. Agent confirms the task is complete
```

**Instructions:**

* Give the agent access only to the folders required for the workflow.
* Validate the input file before processing it.
* Save the generated report to a controlled location.
* Move or delete files only after the required processing is complete.

## Quick Memory

```text
Read → Get data from files
Write → Create or update files
Manage → Organize files and folders
Security → Control what the agent can access
Workflow → Read → Process → Write → Organize
```
