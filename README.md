# EDP Analytics – Power BI Workspace Setup Guide

This repository contains analytics workspaces and Power BI projects for the **EDP Analytics** platform.

This guide walks contributors through:

1. Installing and configuring **GitHub Desktop**
2. Cloning the **`edp-analytics`** repository (devtest branch)
3. Locating a **Power BI (.pbib)** workspace file
4. Connecting the Power BI semantic model to **Databricks SQL Warehouse**

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [1. Install and Configure GitHub Desktop](#1-install-and-configure-github-desktop)
- #2-clone-the-repository-devtest-branch
- [3. Locate the Power BI Workspace File](#3-locate-the-power-bi-workspace-file)
- [4. Connect Power BI to Databricks](#4-connect-power-bi-to-databricks)
- [Troubleshooting](#troubleshooting)
- #screenshot-management
- [Summary](#summary)

---

## Prerequisites

Before starting, ensure you have:

- A **GitHub account** with access to  
  `Childrens-National-Hospital/edp-analytics`
- **Power BI Desktop** installed
- Access to the **team_data_product_management** Databricks SQL Warehouse
- Organizational authentication configured (Azure AD / SSO)

---

## 1. Install and Configure GitHub Desktop

### 1.1 Download GitHub Desktop

Download GitHub Desktop from:

https://desktop.github.com/download/

![GitHub Desktop download page](docs/images/01-github-desktop-download.png)

---

### 1.2 Install GitHub Desktop

Run the installer and complete the setup using default options.

![GitHub Desktop installed](docs/images/02-github-desktop-installed.png)

---

### 1.3 Sign In to GitHub

1. Open **GitHub Desktop**
2. Navigate to:
   - **File → Options → Accounts** (Windows)
   - **GitHub Desktop → Settings → Accounts** (Mac)
3. Click **Sign in to GitHub.com**
4. Complete authentication in your browser

![GitHub Desktop signed in](docs/images/03-github-desktop-signed-in.png)

✅ GitHub Desktop is now connected to your GitHub account.

---

## 2. Clone the Repository (devtest Branch)

Repository URL (devtest branch):

https://github.com/Childrens-National-Hospital/edp-analytics/tree/devtest

---

### 2.1 Clone Using GitHub Desktop

1. Click **Code**
2. Select **Open with GitHub Desktop**
3. Choose a local folder (or accept the default)
4. Click **Clone**

![Open with GitHub Desktop](docs/images/04-github-code-open-desktop.png)
![Clone dialog](docs/images/05-desktop-clone-dialog.png)

---

### 2.2 Verify Branch Selection

In GitHub Desktop, confirm the current branch is:

```text
devtest
