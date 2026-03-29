# WSL Alpine PostgreSQL 15

This repository provides a tarball for running an Alpine-based PostgreSQL 15 instance inside WSL (Windows Subsystem for Linux).

## Prerequisites

- Windows 10 version 2004 or later, or Windows 11
- WSL 2 enabled
- The `wsl_alpine_postgresql_15.tar.gz` tarball (tracked via Git LFS)

## Setup Instructions

Run the following commands in **PowerShell** (run as Administrator):

### 1. Import the Alpine PostgreSQL distribution

```powershell
wsl --import AlpinePostgres C:\wsl\AlpinePostgres .\wsl_alpine_postgresql_15.tar.gz
```

This imports the tarball as a new WSL distribution named `AlpinePostgres`. The distribution's virtual disk will be stored in `C:\wsl\AlpinePostgres`.

### 2. Verify the distribution was imported

```powershell
wsl -l -v
```

This lists all installed WSL distributions and their status. Confirm that `AlpinePostgres` appears in the list.

### 3. Start the distribution

```powershell
wsl -d AlpinePostgres
```

This launches a shell session inside the `AlpinePostgres` distribution where PostgreSQL 15 is available.
