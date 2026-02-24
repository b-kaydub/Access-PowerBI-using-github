EDP Analytics – Power BI Workspace Setup Guide
This repository contains analytics workspaces and Power BI projects for the EDP Analytics platform.
This guide walks contributors through:

Installing and connecting GitHub Desktop
Cloning the edp-analytics repository (devtest branch)
Locating a Power BI (.pbib) workspace file
Connecting the Power BI semantic model to Databricks SQL Warehouse


Table of Contents

#prerequisites
#1-install-and-configure-github-desktop
#2-clone-the-repository-devtest-branch
#3-locate-the-power-bi-workspace-file
#4-connect-power-bi-to-databricks
#troubleshooting
#screenshot-management
#summary


Prerequisites
Before starting, ensure you have:

A GitHub account with access to
Childrens-National-Hospital/edp-analytics
Power BI Desktop installed
Access to the team_data_product_management Databricks SQL Warehouse
Organizational authentication configured (Azure AD / SSO)


1. Install and Configure GitHub Desktop
1.1 Download GitHub Desktop
Download GitHub Desktop from:
https://desktop.github.com/
docs/images/01-github-desktop-download.png

1.2 Install GitHub Desktop
Run the installer and complete the setup using default options.
docs/images/02-github-desktop-installed.png

1.3 Sign In to GitHub

Open GitHub Desktop
Navigate to:

File → Options → Accounts (Windows)
GitHub Desktop → Settings → Accounts (Mac)


Select Sign in to GitHub.com
Complete browser authentication

docs/images/03-github-desktop-signed-in.png
✅ GitHub Desktop is now connected to your GitHub account.

2. Clone the Repository (devtest Branch)
Repository URL (devtest branch):
https://github.com/Childrens-National-Hospital/edp-analytics/tree/devtest

2.1 Clone Using GitHub Desktop

Click Code
Select Open with GitHub Desktop
Choose a local folder (or accept the default)
Click Clone

docs/images/04-github-code-open-desktop.png
docs/images/05-desktop-clone-dialog.png

2.2 Verify Branch Selection
In GitHub Desktop, confirm the current branch is:
devtest

If needed:

Click Current Branch
Select devtest

docs/images/06-branch-devtest.png

3. Locate the Power BI Workspace File
3.1 Open the Repository Locally
In GitHub Desktop:

Repository → Show in Explorer (Windows)
Repository → Show in Finder (Mac)

docs/images/07-show-in-explorer.png

3.2 Navigate to the Workspaces Directory
edp-analytics/
└── workspaces/

docs/images/08-workspaces-folder.png
Repository reference:
https://github.com/Childrens-National-Hospital/edp-analytics/tree/devtest/workspaces

3.3 Identify the .pbib File
Within workspaces/, locate the Power BI Project file:
*.pbib

Example:
edp_workspace.pbib

docs/images/09-pbib-highlight.png

4. Connect Power BI to Databricks
4.1 Open the Power BI Project
Open the .pbib file by:

Double‑clicking the file, or
Right‑click → Open with → Power BI Desktop

docs/images/10-powerbi-opened.png

4.2 Open Data Source Settings
In Power BI Desktop:

Select Transform data
Choose Data source settings

docs/images/11-data-source-settings.png

4.3 Update the Databricks Connection

Select the existing Databricks connection
Click Change Source

docs/images/12-change-source.png

4.4 Enter Databricks SQL Warehouse Details
Use the following connection details:
Server Hostname
adb-4066047606628959.19.azuredatabricks.net

HTTP Path
/sql/1.0/warehouses/6372a0a3911012ac

Data Source Type
Azure Databricks

docs/images/13-databricks-host-path.png

4.5 Authenticate
When prompted:

Choose Microsoft account / Azure Active Directory
Sign in with your organizational credentials

docs/images/14-authentication.png

4.6 Apply Changes and Refresh

Click Close & Apply
Select Refresh

docs/images/15-refresh.png
✅ If successful, report visuals will populate using Databricks data.

Troubleshooting





















IssueResolutionAuthentication failureConfirm Databricks SQL Warehouse accessMissing tables or viewsVerify default catalog and schemaRefresh errorsRe‑check hostname and HTTP path
docs/images/16-error-example.png

Screenshot Management
Screenshots referenced in this README are stored in:
docs/images/

Guidelines

Use .png format
Avoid exposing credentials or tokens
Blur or redact sensitive identifiers
Follow this naming pattern:
01-github-desktop-download.png
02-github-desktop-installed.png
03-github-desktop-signed-in.png
...




Summary
You have now:
✅ Installed and configured GitHub Desktop
✅ Cloned the edp-analytics repository (devtest branch)
✅ Located a Power BI workspace project
✅ Connected the semantic model to Databricks SQL Warehouse
You are ready to develop and analyze Power BI content backed by Databricks.
