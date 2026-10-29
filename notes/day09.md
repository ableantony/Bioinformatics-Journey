# Day 09 - 27/10/2026

## Linux: cat, head, tail

### cat

- Reads a file and displays its text on the screen.
  ```bash
  cat file.txt
  ```
- Can make a new file and add text to it straight away. Type the text, then press Ctrl + D to save and finish.
  ```bash
  cat > file.txt
  ```
- Can add new text on the next line of a file that already exists. Type the text, then press Ctrl + D.
  ```bash
  cat >> file.txt
  ```

### head

- Displays the first 10 lines of any file that can be shown as text.
  ```bash
  head file.txt
  ```
- Number modifier `-n` chooses how many lines are displayed.
  ```bash
  head -n 5 file.txt
  ```
- Modifier `-c` chooses how many bytes' worth of content is displayed.
  ```bash
  head -c 50 file.txt
  ```

### tail

- Same as head, but for the last lines of a text file (last 10 by default).
  ```bash
  tail file.txt
  ```
- Same modifiers as head: `-n` for the number of lines, `-c` for bytes.
  ```bash
  tail -n 3 file.txt
  tail -c 50 file.txt
  ```
- Modifier `-f` keeps tail running so that new lines added to the file show up as they are written. Press Ctrl + C to stop it.
  ```bash
  tail -f file.txt
  ```

## Summary

| Command | Use |
|---|---|
| `cat file` | display a file |
| `cat > file` | create a file and add text |
| `cat >> file` | add text to the next line of an existing file |
| `head -n N file` | first N lines |
| `head -c N file` | first N bytes |
| `tail -n N file` | last N lines |
| `tail -c N file` | last N bytes |
| `tail -f file` | keep following new lines |
