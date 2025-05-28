# Standard Output (stdout)

## Overview
Standard output (stdout) is the default output stream for processes in Linux. By default, most commands send their output to the screen, but this can be redirected.

## Basic Output
The `echo` command demonstrates basic stdout:
```bash
$ echo Hello World    # Displays "Hello World" on screen
```

When you run this command:
1. Input comes from keyboard (stdin)
2. Output goes to screen (stdout)

## Output Redirection
### The > Operator
- Redirects stdout to a file
- Creates new file if it doesn't exist
- Overwrites existing file content

Example:
```bash
$ echo Hello World > peanuts.txt    # Creates/overwrites peanuts.txt
```

### The >> Operator
- Appends stdout to a file
- Creates new file if it doesn't exist
- Preserves existing content

Example:
```bash
$ echo Hello World >> peanuts.txt    # Appends to peanuts.txt
```

## Important Notes
1. The `>` operator will overwrite files without warning
2. Some shells offer protection flags against overwriting
3. Use `>>` when you want to preserve existing file content
