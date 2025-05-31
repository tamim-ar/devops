# Linux Command Line Reference

## 1. System Navigation
### Current Location
#### pwd (Print Working Directory)
- Shows your current location in the filesystem
- Example: `pwd`
- Output: `/home/user/documents`

### Directory Movement
#### cd (Change Directory)
- `.` represents current directory
- `..` moves up one directory
- `~` represents home directory
- `-` returns to previous directory

Examples:
```bash
cd .     # Stay in current directory
cd ..    # Move up one directory level
cd ~     # Go to home directory
cd -     # Go to previous directory
```

### Directory Listing
#### ls (List Directory Contents)
Basic listing variations:
```bash
ls        # List current directory contents
ls /pete  # List contents of /pete directory
ls -a     # Show all files (including hidden)
ls -l     # Long format listing
ls -la    # Combination of -l and -a
```

Details:
1. `ls` - Shows visible files and directories
2. `ls /path` - Lists contents of specific directory
3. `ls -a` - Shows hidden files (starting with .)
4. `ls -l` - Shows detailed information including:
   - Permissions
   - Number of links
   - Owner
   - Group
   - Size
   - Date/time
   - Name
5. `ls -la` - Combines long format with hidden files

## 2. File Management
### File Creation and Identification
#### touch
- Creates empty files or updates timestamps
- Example: `touch myfirstsuperduperfile`
- Use cases:
  1. Create new empty files
  2. Update file access times
  3. Create multiple files at once

#### file
- Determines file type by examining content
- Shows MIME type and additional details
- Useful for files without extensions

Examples:
```bash
$ file banana.jpg     # Output: banana.jpg: JPEG image data, JFIF standard 1.01
$ file /bin/bash      # Output: /bin/bash: ELF 64-bit LSB executable
$ file index.html     # Output: index.html: HTML document, ASCII text
```

Use cases:
1. Verify file types before processing
2. Debug file extension mismatches
3. Identify unknown/corrupted files

### File Content Viewing
#### cat (Concatenate)
- Displays content of files
- Can display multiple files at once
```bash
$ cat dogfile birdfile    # Shows contents of both files together
```

#### less (Pager)
- Views file contents page by page
- More advanced than `more` command
```bash
$ less /home/pete/Documents/text1
```

Navigation in less:
- `q` - Quit and return to shell
- `Page up/down` - Navigate pages
- `Up/Down arrows` - Navigate lines
- `g` - Go to beginning
- `G` - Go to end
- `/search` - Search for text
- `h` - Display help

### File Operations
#### cp (Copy)
- Copies files and directories
- Common options:
  - `-i` Interactive mode (prompts before overwriting)
  - `-r` Recursive copy (for directories)

Examples:
```bash
$ cp -i mycoolfile /home/pete/Pictures      # Copy with overwrite confirmation
$ cp -r Pumpkin/ /home/pete/Documents       # Copy directory recursively
$ cp *.jpg /home/pete/Pictures              # Copy all jpg files
$ cp mycoolfile /home/pete/Documents/cooldocs   # Copy to specific location
```

#### mv (Move/Rename)
- Moves or renames files and directories
- Common options:
  - `-i` Interactive mode (prompts before overwrite)
  - `-b` Creates backup of existing files

Examples:
```bash
$ mv oldfile newfile                    # Rename a file
$ mv file2 /home/pete/Documents         # Move a file
$ mv file_1 file_2 /somedirectory      # Move multiple files
$ mv directory1 directory2              # Move/rename directory
$ mv -i directory1 directory2           # Move with overwrite confirmation
$ mv -b directory1 directory2           # Move with backup creation
```

### Directory Management
#### mkdir (Make Directory)
- Creates new directories
- Common options:
  - `-p` Create parent directories as needed

Examples:
```bash
$ mkdir books paintings              # Create multiple directories
$ mkdir -p books/hemmingway/favorites    # Create nested directories
```

#### rm and rmdir (Remove)
- Removes files and directories
- Common options:
  - `-f` Force removal without confirmation
  - `-i` Interactive mode (prompt before removal)
  - `-r` Recursive removal (for directories)

Examples:
```bash
$ rm file1                  # Remove a file
$ rm -f file1              # Force remove without confirmation
$ rm -i file               # Remove with confirmation
$ rm -r directory          # Remove directory and contents
$ rmdir directory          # Remove empty directory only
```

### File Search
#### find
- Searches for files and directories
- Common options:
  - `-name` Search by name
  - `-type` Search by type (f for files, d for directories)

Examples:
```bash
$ find /home -name puppies.jpg          # Find file by name
$ find /home -type d -name MyFolder     # Find directory by name
```

## 3. System Utilities
### Help and Documentation
#### help
- Shows help information for commands
- Two common ways to get help:
  1. Using `help` command
  2. Using `--help` option

Examples:
```bash
$ help echo              # Built-in command help
$ echo --help           # Command-specific help option
```

#### man (Manual)
- Displays system manual pages
- Provides detailed documentation for commands
- Press 'q' to exit the manual page

Example:
```bash
$ man ls                # Show manual for ls command
```

#### whatis
- Shows one-line manual page descriptions
- Quick way to get command purpose
- Similar to man but more concise

Example:
```bash
$ whatis cat            # Shows brief description of cat command
```

### Terminal Management
#### clear
- Clears terminal screen
```bash
$ clear
```

#### history
- Shows command history
- Lists previously executed commands
```bash
$ history
```

### Session Control
#### alias and unalias
- Creates or removes command shortcuts
- Can be made persistent in ~/.bashrc
- Commonly used for command customization

Examples:
```bash
$ alias foobar='ls -la'     # Create alias for ls -la
$ unalias foobar           # Remove the alias
```

> Note: Add aliases to ~/.bashrc file to make them permanent

#### exit and logout
- Terminates current shell session
- Both commands perform similar functions
- Common for ending terminal sessions

Examples:
```bash
$ exit                # Exit current shell
$ logout             # Log out of current session
```

## 4. Common Use Cases
1. View multiple files:
```bash
$ cat file1 file2 file3
```

2. Read long files:
```bash
$ less large_log_file.txt
```

3. Clear screen for better visibility:
```bash
$ clear
```

4. Check recent commands:
```bash
$ history | less
```
