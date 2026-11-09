# File Management Tool

A Python-based file handler that mimics a Windows-style command prompt. It allows users to navigate directories, list drives, read and copy files, search for terms, and manage a custom recycle bin for safe file deletion and recovery.

## Features
- Directory navigation and drive listing
- File reading and copying
- Content search within files
- Custom recycle bin with recovery support

## Requirements
- Python 3.x
- Additional packages may be needed for full functionality (pygments, python-docx)

## How to Run
```bash
python main.py.py
```

## User Manual

### Starting the Program
1. Open a terminal/command prompt.
2. Navigate to the project folder.
3. Run: `python main.py.py`
4. You will see a command prompt showing your current directory.

### Available Commands
Type a command and press Enter. Type `help` anytime to see this list.

| Command | Usage | Description |
|---------|-------|-------------|
| `dir` | `dir` | List files and folders in the current directory. |
| `cd` | `cd [path]` or `cd ..` or `cd D:` | Change directory, go up one level, or switch drives. |
| `type` | `type filename.txt` | Display the contents of a text file. |
| `drives` | `drives` | Show all available drives on the system. |
| `copy` | `copy` | Start interactive file copy (prompts for source and destination). |
| `read` | `read` | Read or open a file based on its type (code, docx, pdf, etc.). |
| `search` | `search` | Search for a term or regex pattern inside files. |
| `delete` | `delete` | Move a file to the custom recycle bin or recover a file from it. |
| `help` | `help` | Show the list of available commands. |
| `exit` | `exit` | Close the program. |

### Command Details

**Navigation**
- `dir` — Shows directories as `<DIR>` and files with their names.
- `cd foldername` — Enter a folder.
- `cd ..` — Go back one folder.
- `cd D:` — Switch to drive D.

**File Operations**
- `type notes.txt` — Print the contents of a text file.
- `copy` — You will be asked for the full source path and full destination path (including new filename).
- `read` — Prompts for a filename. Supports code files (syntax highlighting), `.docx`, and `.pdf`.

**Search**
- `search` — Asks for base directory, subdirectory, search term, and whether to search recursively.

**Recycle Bin**
- `delete` — Choose 1 to delete (moves to recycle bin) or 2 to recover a file by name.

### Example Session
```
C:\Users\You\Desktop> dir

 Directory of C:\Users\You\Desktop

<DIR>        Projects
             notes.txt

C:\Users\You\Desktop> type notes.txt
----------------------------------------
Hello World
----------------------------------------

C:\Users\You\Desktop> help

Available Commands:
  dir             List directory contents
  cd [path]       Change the current directory...
  ...

C:\Users\You\Desktop> exit
Exiting File Navigator.
```

### Tips
- The recycle bin is stored in your home folder as `.recycle_bin`.
- Paths can be relative to the current directory or full paths.
- Unsupported file types for `read` will show a message.

## Project Structure
- `main.py.py` - Main entry point
- `FMT_1_reader.py.py` - File reading module
- `FMT_2_Copying_txt.py` - File copying
- `FMT_3_File_Searcher.py` - Search functionality
- `FMT_5_File_Recovery .py` - Recycle bin recovery

## License
GPL-3.0
