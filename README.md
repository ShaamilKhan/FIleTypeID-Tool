# Magic File Scanner

Detects the TRUE file type of any file using magic number analysis.
Flags disguised malware — e.g. a Windows EXE renamed as vacation_photo.jpeg.

## What are Magic Numbers?
Every file type has a secret signature hidden in its first few bytes.
A JPEG always starts with FF D8 FF. A Windows EXE always starts with 4D 5A.
This tool reads those bytes and compares them against a database of 25+ file types,
regardless of what the file extension claims.

## Features
- Detects 25+ file types (images, executables, archives, documents, media)
- Flags extension mismatches that indicate disguised malware
- ASCII terminal UI with live scan animation
- Scan a single file or an entire folder recursively

## How to Run
python magic_file_scanner_ui.py --demo
python magic_file_scanner_ui.py /path/to/folder
python magic_file_scanner_ui.py suspicious.jpeg -v

## Example Output
[ !! ]  vacation_photo.jpeg  [.jpeg]  108 B
Status   | MISMATCH — POSSIBLE MALWARE DISGUISE
Detected | EXE/DLL (Windows PE)
Expected | JPEG
/!\  WARNING: This is a known malware evasion technique.

## Requirements
- Python 3.10+ (no external libraries needed)

## Author
Shaamil Khan A
```
*.class
demo_files/
.DS_Store
