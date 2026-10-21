# Day 3: Working with Files (Linux)(21/10/2026)

**Focus:** File commands in the Linux terminal (WSL2 Ubuntu)
**Status:** Complete.

---

## Summary

Hands-on Linux practice. I learned the file commands, hit real errors, fixed them myself, and finished a full exercise ("Tidy the sequencing lab") that used everything learned so far.

---

## Commands learned

| Command | What it does | Notes |
|---|---|---|
| `touch file` | Creates an empty file | On an existing file it only updates the timestamp; contents are untouched |
| `file name` | Identifies the type of a file | Examines the contents, not just the extension; works on folders too (`directory`) |
| `cp a b` | Copies a file | Use `cp -r folder copy` to copy a folder and everything in it |
| `mv a b` | Moves or renames | Moves into a folder if `b` is a folder; silently overwrites an existing destination; no `-r` needed for folders |
| `rm file` | Deletes a file permanently | No recycle bin; refuses folders unless `-r`; `rm -i` asks first |

Also practiced: `pwd`, `cd`, `ls`, `ls -R`, `mkdir`, `echo`, and chaining commands with `&&`.

### Overwrite vs append

```bash
echo "ATGGTA" > seq1.txt     # > overwrites the whole file
echo "CCGATT" >> seq1.txt    # >> appends a new line at the end
```

### `mv` patterns

```bash
mv A B              # rename A to B (if B is not a folder)
mv A folder/        # move A into folder, same name
mv A folder/B       # move A into folder and rename it B
mv A B C folder/    # move several files (last word must be a folder)
```

---

## Exercise report: "Tidy the sequencing lab"

**Result:** Complete.

Tasks done:

- Built `messylab` with six files, three holding short DNA sequences
- Made `data`, `backup`, `results`
- Renamed sample files to `seq1.txt`, `seq2.txt`, `seq3.txt` and moved them into `data`
- Appended a second DNA line to each file
- Copied `data` into `backup` with `cp -r`
- Created `results/summary.txt`
- Deleted temp files with `rm -i`, then deleted the old notes file
- Used `file` on files and on the folder
- Walked through every folder and listed its contents
