# Technical Specifications & Data Privacy — CutoverCheck by JE Horizon

## Architectural Principles

1. **Local-First Execution:** All business logic, calculation engines, and file operations execute directly on the local machine.
2. **Zero Telemetry:** The application does not include third-party tracking pixels, behavioural analytics, or background telemetry beacons.
3. **Storage Isolation:** Application data is stored in the user's isolated local app directory using secure local storage (SQLite with atomic write transactions, Windows DPAPI encryption).
4. **Resilient Offline Operation:** Full functionality remains accessible without an active internet connection.

## Key Feature Matrix

### Capture a read-only baseline from selected folders and exclusions.

Operates entirely within local process memory and writes directly to local storage.
### Map source folders to destination folders across systems.

Operates entirely within local process memory and writes directly to local storage.
### Compare selected file hashes (SHA-256) after a migration.

Operates entirely within local process memory and writes directly to local storage.
### Keep manual application attestations separate from measured file results.

Operates entirely within local process memory and writes directly to local storage.
### Export local HTML handoff reports with full-detail or summary-only views.

Operates entirely within local process memory and writes directly to local storage.


## Security & Integrity

- **Database Engine:** Embedded SQLite with Write-Ahead Logging (WAL) and foreign-key constraints.
- **Data Boundaries:** Zero customer data is uploaded to remote servers during regular usage.
