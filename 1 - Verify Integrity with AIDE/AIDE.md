# What is AIDE?
AIDE (Advanced Intrusion Detection Environment) is an open-source file integrity checker and intrusion detection system for Unix-like operating systems. It helps administrators detect unauthorized changes to the filesystem, which can be an indicator of a security breach.

## Key Points about AIDE:
### 1. Purpose:

AIDE monitors and verifies the integrity of the system files by creating a database of file attributes and then comparing the current state of the files against this database.

### 2. How It Works:

**Initial Database Creation**: When AIDE is first installed, it scans the filesystem and creates a baseline database of file attributes, such as permissions, timestamps, sizes, and checksums.

**Regular Checks**: During regular checks, AIDE compares the current file attributes against the baseline database to detect any changes.

**Reports**: Any discrepancies found are reported to the system administrator, who can then investigate further.

### 3. Configuration:

AIDE is highly configurable through its configuration file, typically located at **/etc/aide/aide.conf**. This file specifies which directories and files to monitor and what attributes to check.

### 4. Common Use Cases:

**Intrusion Detection**: Detect unauthorized changes to system files that may indicate a security breach.

**Integrity Verification**: Ensure that critical system files remain unchanged and have not been tampered with.
