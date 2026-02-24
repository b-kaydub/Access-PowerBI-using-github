# EDP Analytics – Power BI Workspace Setup Guide

This repository contains analytics workspaces and Power BI projects for the **EDP Analytics** platform.

This guide walks contributors through:

1. Installing and configuring **GitHub Desktop**
2. Cloning the **`edp-analytics`** repository (**devtest** branch)
3. Locating **Power BI (.pbib)** workspace files
4. Connecting the Power BI semantic model to **Databricks SQL Warehouse**
---

## Table of Contents

- [Prerequisites](#prerequisites)
- [1. Install and Configure GitHub Desktop](#1-install-and-configure-github-desktop)
- [2. Clone the Repository (devtest Branch)](#2-clone-the-repository-devtest-branch)
- [3. Locate Power BI Workspace Files](#3-locate-power-bi-workspace-files)
- [4. Connect Power BI to the Databricks Semantic Layer](#4-connect-power-bi-to-the-databricks-semantic-layer)
- [Troubleshooting](#troubleshooting)
- [Screenshot Management](#screenshot-management)
- [Summary](#summary)
---

## Prerequisites

Before starting, ensure you have:

- A **GitHub account** with access to `Childrens-National-Hospital/edp-analytics`
- **Power BI Desktop** installed
- Access to the **team_data_product_management** Databricks SQL Warehouse
- Organizational authentication configured (Azure Active Directory / SSO)

---

## 1. Install and Configure GitHub Desktop

### 1.1 Download GitHub Desktop

Download GitHub Desktop from:

- https://desktop.github.com/download/
---

### 1.2 Install GitHub Desktop

1. Run the installer
2. Accept default installation settings
3. Launch GitHub Desktop after installation completes

![GitHub Desktop download page](docs/images/01-github-desktop-download.png)
---

### 1.3 Sign In to GitHub

1. Open **GitHub Desktop**
2. Navigate to:
   - **File → Options → Accounts** (Windows)
   - **GitHub Desktop → Settings → Accounts** (Mac)
3. Click **Sign in to GitHub.com**
4. Complete authentication in your browser



✅ GitHub Desktop is now connected to your GitHub account.

---

## 2. Clone the Repository (devtest Branch)

Repository URL (devtest branch):

![GitHub Desktop download page](docs/images/04-github-code-oipen-desktop.png)

---

### 2.1 Clone Using GitHub Desktop

1. In your browser, click **Code**
2. Select **Open with GitHub Desktop**
3. Choose a local folder (or accept the default)
4. Click **Clone**

![GitHub Desktop download page](docs/images/05-github-desktop-branch.png)

---

### 2.2 Verify Branch Selection

In GitHub Desktop, confirm the active branch is:

```text
devtest
```

If not:

1. Click **Current Branch**
2. Select **devtest**

**Screenshot (optional):** `docs/images/06-branch-devtest.png`

---

## 3. Locate Power BI Workspace Files

### 3.1 Open the Repository Locally

In GitHub Desktop:

- **Repository → Show in Explorer** (Windows)
- **Repository → Show in Finder** (Mac)

**Screenshot (optional):** `docs/images/07-show-in-explorer.png`

---

### 3.2 Navigate to the Workspaces Directory

Workspace files are stored under:

```text
edp-analytics/
└── workspaces/
```

**Screenshot (optional):** `docs/images/08-workspaces-folder.png`

GitHub reference:

- https://github.com/Childrens-National-Hospital/edp-analytics/tree/devtest/workspaces

---

### 3.3 Identify the Power BI Project File (.pbib)

Within the `workspaces/` directory, locate a file ending in:

```text
.pbib
```

Example:

```text
edp_workspace.pbib
```

**Screenshot (optional):** `docs/images/09-pbib-highlight.png`

This `.pbib` file typically contains:

- Power BI report definition
- Semantic model definition
- Connection metadata (including data sources)

---

## 4. Connect Power BI to the Databricks Semantic Layer

### 4.1 Open the Power BI Project

Open the `.pbib` file by:

- Double‑clicking the file
- **OR** Right‑click → **Open with → Power BI Desktop**

**Screenshot (optional):** `docs/images/10-powerbi-opened.png`

---

### 4.2 Open Data Source Settings

In Power BI Desktop:

1. Select **Transform data**
2. Click **Data source settings**

**Screenshot (optional):** `docs/images/11-data-source-settings.png`

---

### 4.3 Update the Databricks Connection

1. Select the existing **Databricks** data source
2. Click **Change Source**

**Screenshot (optional):** `docs/images/12-change-source.png`

---

### 4.4 Enter Databricks SQL Warehouse Connection Details

Use the following values exactly:

**Server Hostname**

```text
adb-4066047606628959.19.azuredatabricks.net
```

**HTTP Path**

```text
/sql/1.0/warehouses/6372a0a3911012ac
```

**Data Source Type**

```text
Azure Databricks
```

**Screenshot (optional):** `docs/images/13-databricks-host-path.png`

This connects the semantic model to the **team_data_product_management** SQL Warehouse.

---

### 4.5 Authenticate

When prompted:

- Select **Microsoft account / Azure Active Directory**
- Sign in using your organizational credentials

**Screenshot (optional):** `docs/images/14-authentication.png`

---

### 4.6 Apply Changes and Refresh

1. Click **Close & Apply**
2. Click **Refresh**

**Screenshot (optional):** `docs/images/15-refresh.png`

✅ If successful, report visuals will populate using data from Databricks.

---

## Troubleshooting

| Issue | Resolution |
|------|------------|
| Authentication failure | Confirm you have access to the Databricks SQL Warehouse (and re-authenticate in **Data source settings → Edit Permissions**) |
| Missing tables/views | Verify the correct catalog and schema are used (and that your identity has access) |
| Refresh errors | Re-check the **Server Hostname** and **HTTP Path** for typos |

**Screenshot (optional):** `docs/images/16-error-example.png`

---

## Screenshot Management

Recommended screenshot folder:

```text
docs/images/
```

Guidelines:

- Use `.png` format
- Do not expose credentials, tokens, or private identifiers
- Blur/redact sensitive info before committing
- Suggested naming convention:

```text
01-github-desktop-download.png
02-github-desktop-installed.png
03-github-desktop-signed-in.png
...
```

---

## Summary

You have now:

- ✅ Installed and configured GitHub Desktop
- ✅ Cloned the `edp-analytics` repository (`devtest` branch)
- ✅ Located Power BI workspace `.pbib` files
- ✅ Connected the semantic model to the Databricks SQL Warehouse

You are ready to develop and analyze Power BI content backed by Databricks.

