# 🗂️ Automated File Organizer

A Python automation script that moves all files of a specific type (for example `.jpg`) from a source folder to a destination folder.

## Features
- Creates the destination folder if it doesn't exist
- Case-insensitive extension matching (`.JPG` and `.jpg`)
- Moves only files, not subfolders
- Handles errors per file and prints a summary of how many files were moved

## Concepts Used
- `os` module (`listdir`, `path.join`, `makedirs`, `isfile`)
- `shutil` module (`move`)
- Functions with default parameters
- Exception handling

## How to Use
```python
from file_organizer import organize_files

organize_files("C:/Users/You/Downloads", "C:/Users/You/Pictures/Organized", ".jpg")
```

Or add this at the bottom of the file and run `python file_organizer.py`:
```python
if __name__ == "__main__":
    organize_files("source_folder", "destination_folder", ".jpg")
```

## Sample Output
```
Created destination folder: Organized
Scanning source folder: Downloads
Moved: photo1.jpg
Moved: photo2.JPG
===================================
✅ Automation Complete: 2 .jpg file(s) moved.
===================================
```

## Future Improvements
- Auto-sort into folders by file type (images, docs, videos)
- Command-line arguments with `argparse`
- Handle duplicate file names

## Author
[Your Name] | CodeAlpha Python Programming Internship
