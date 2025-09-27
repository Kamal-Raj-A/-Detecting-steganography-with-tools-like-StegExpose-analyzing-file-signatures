# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
<img width="749" height="967" alt="Screenshot 2025-09-27 205838" src="https://github.com/user-attachments/assets/19cb5f62-1a64-4821-94a0-d942c62a27e4" />
<img width="749" height="995" alt="Screenshot 2025-09-27 205852" src="https://github.com/user-attachments/assets/759f3f2d-98e3-4780-a9bf-85afc9ec9017" />
<img width="760" height="1005" alt="Screenshot 2025-09-27 205751" src="https://github.com/user-attachments/assets/92febe2a-2807-42c6-be8a-415d7e91f522" />
<img width="757" height="1005" alt="Screenshot 2025-09-27 205807" src="https://github.com/user-attachments/assets/dde25f3d-2be2-46d4-a5f1-3eaaf1440cca" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
