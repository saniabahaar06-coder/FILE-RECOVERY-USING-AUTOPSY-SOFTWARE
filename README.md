# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1636" height="858" alt="Screenshot 2026-09-07 225302" src="https://github.com/user-attachments/assets/116f07fe-307c-4622-bae0-6cb88ba1beb5" />
<img width="1621" height="852" alt="Screenshot 2026-09-07 225329" src="https://github.com/user-attachments/assets/6328d6bf-cd15-463f-9d5b-4b5dea273f58" />

<img width="1632" height="865" alt="Screenshot 2026-09-07 225402" src="https://github.com/user-attachments/assets/252a262b-d876-40a2-b980-b379505d2c4e" />
<img width="1625" height="861" alt="Screenshot 2026-09-07 225418" src="https://github.com/user-attachments/assets/4fbaedbd-9b7e-472d-bb46-a48812b0082c" />

<img width="1642" height="855" alt="Screenshot 2026-09-07 225437" src="https://github.com/user-attachments/assets/d1e58d93-b99b-4043-a7f7-d3f410271c86" />
<img width="1640" height="865" alt="Screenshot 2026-09-07 225500" src="https://github.com/user-attachments/assets/a41bfb24-2fee-4d28-a14e-c15805b115c8" />




## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
