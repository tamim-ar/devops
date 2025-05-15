# Basic Linux Navigation Commands

## 1. Current Directory Commands
### pwd (Print Working Directory)
- Shows your current location in the filesystem
- Example: `pwd`
- Output: `/home/user/documents`

### cd (Change Directory)
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

## 2. Directory Listing Commands
### ls (List Directory Contents)
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

## 3. File Creation
### touch
- Creates empty files or updates timestamps
- Example: `touch mysuperduperfile`
- Use cases:
  1. Create new empty files
  2. Update file access times
  3. Create multiple files at once
