# Linux File Viewing and System Commands

## 1. File Content Commands
### cat (Concatenate)
- Displays content of files
- Can display multiple files at once
```bash
$ cat dogfile birdfile    # Shows contents of both files together
```

### less (Pager)
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

## 2. System Commands
### clear
- Clears terminal screen
```bash
$ clear
```

### history
- Shows command history
- Lists previously executed commands
```bash
$ history
```

## Common Use Cases
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