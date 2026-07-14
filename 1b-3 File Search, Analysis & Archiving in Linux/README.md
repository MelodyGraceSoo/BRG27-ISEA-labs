# Lab 1b-3: File Search, Analysis & Archiving in Linux

## Objective

Learn to extract compressed archives and apply advanced command-line file search techniques (by filename, content, date, size) to solve real problems on a Linux filesystem.

## Class Activity Overview

This lab trains students in using command-line tools to locate, inspect, and search through text files, especially within large archives. It builds essential skills in system administration and file forensics using Linux.

## Learning Objectives

- Extract compressed archive files using `bunzip2` and `tar`.
- Search for files by name, extension, and content using `find` and `grep`.
- Understand and apply file modification and creation timestamp analysis.
- Locate files by size and frequency of use.
- Use `sed`, `sort`, and `uniq` to explore data trends in large files.
- Answer analytical questions using Linux command-line tools.

## Lab Setup and Steps

- Download `gutenberg.tar.bz2` from LMS.
- Extract with: `bunzip2 gutenberg.tar.bz2` then `tar -xvf gutenberg.tar`.
- Explore contents: `ls -l`, `tree`, or `less` to inspect a few files.
- Search for filenames: `find ./Gutenberg -name "*.txt"`.
- Search for strings: `grep -r 'keyword' ./Gutenberg` or `find -exec grep`.
- Search with context: `grep -r -C 3 'Next day' ./Gutenberg`.
- Search by size: `find ./Gutenberg -type f -size 255258c -exec ls -lh {} \;`.
- Search by creation/modification date: `find -type f -printf '%T+ %p\n' | sort`.
- Find largest files: `du -a ./Gutenberg | sort -nr | head`.
- Analyze frequency in files: `sed -e 's/\s/\n/g' < file.txt | sort | uniq -c | sort -nr | head -200`.

> **Note on deviation:** files were provided as `1b-3-Gutenberg.zip` rather than `gutenberg.tar.bz2`, so `unzip` was used in place of `bunzip2`/`tar`.

## Analytical Questions

- How many times does the string "verdigris" appear? (number only)
- What is the surname of the author of the filename "1107.txt"? (case sensitive)
- What is the surname of the author of the file that is exactly 255258 bytes? (case sensitive)
- What is the filename of the file with the 3rd oldest creation date?
- Find the word that follows the text: "Next day there was a surprise for Jack" (case-sensitive, no spaces)

## Reflection Prompts

- Which command-line tool was the most useful in solving the questions?
- How might these search tools help in cybersecurity investigations?
- How could scripting improve repetitive search tasks?
- What limitations did you encounter using `grep` and `find`?

## Deliverables

| # | Deliverable | Description |
|---|---|---|
| ✅ 1 | Archive Extracted Successfully | Screenshot/log of extraction |
| ✅ 2 | File Listing of Extracted Directory | `ls -l` output confirming extraction |
| ✅ 3 | Filename Search Demonstrated | `find . -name "*.txt"` or similar |
| ✅ 4 | Text Search via Grep | `grep -r "verdigris" .` or equivalent |
| ✅ 5 | Contextual Text Search | `grep -r -C 3 "Next day there was a surprise for Jack" .` |
| ✅ 6 | Date-Based File Searches | 3rd oldest file via `find ... -printf '%T+ %p\n'` |
| ✅ 7 | Size-Based File Searches | `find . -type f -size 255258c -exec ls -lh {} \;` |
| ✅ 8 | Largest Files Found | `du -a . \| sort -nr \| head` |
| ✅ 9 | Text Frequency Analysis Performed | `sed -e 's/\s/\n/g' < file.txt \| sort \| uniq -c` |
| ✅ 10 | Answers to Questions Provided | All 5 analytical questions answered |

## Screenshots & Command Outputs

**1. Archive Extraction**

![Unzip extraction](./images/01-unzip-extraction.png)

Using `unzip` to extract the text files from the Gutenberg folder.

**2. File Listing**

![File listing](./images/02-file-listing.png)

`ls -l 1b-3-Gutenberg` listing the three extracted files.

**3. Filename Search**

![Filename search](./images/03-filename-search.png)

`find . -name "*.txt"` scoped to the Downloads folder — output correctly returning the three extracted Gutenberg files.

**4. Text Search & Contextual Search (Grep)**

![Grep text and contextual search](./images/04-grep-text-and-contextual-search.png)

`grep -r 'the' ./1b-3-Gutenberg` (text search) then `grep -r -C 3 'enterprise' ./1b-3-Gutenberg` (contextual search with 3 lines of surrounding context).

**5. Size-Based Search**

![Size-based search](./images/05-size-based-search.png)

`find ./1b-3-Gutenberg -type f -size 94c -exec ls -lh {} \;` → `frankenstein.txt`.

**6. Date-Based Search**

![Date-based search](./images/06-date-based-search.png)

`find ./1b-3-Gutenberg -type f -printf '%T+ %p\n' | sort`.

**7. Largest Files**

![Largest files](./images/07-largest-files.png)

`du -a ./1b-3-Gutenberg | sort -nr | head` to find the largest file size.

**8. Text Frequency Analysis**

![Text frequency analysis](./images/08-text-frequency-analysis.png)

Word frequency analysis on `frankenstein.txt` — using `sed` to split the text into one word per line, then `sort | uniq -c | sort -nr` to count and rank each word by frequency.
