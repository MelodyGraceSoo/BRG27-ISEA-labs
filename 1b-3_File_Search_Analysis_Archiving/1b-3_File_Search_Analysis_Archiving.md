# File Search, Analysis & Archiving in Linux

![Using unzip to extract the text files from the Gutenberg folder](./images/01-unzip-extract.png)

Using unzip to extract the text files from the Gutenberg folder

![ls -l 1b-3-Gutenberg listing the three extracted files](./images/02-ls-listing.png)

`ls -l 1b-3-Gutenberg` listing the three extracted files

![Performing find . -name "*.txt" in the Downloads folder](./images/03-find-filename-search.png)

Performing `find . -name "*.txt"` in the Downloads folder — output correctly returning the three extracted Gutenberg files (Filename search)

![grep -r 'the' text search then grep -r -C 3 'enterprise' contextual search](./images/04-grep-text-search.png)

`grep -r 'the' ./1b-3-Gutenberg` (text search) then `grep -r -C 3 'enterprise' ./1b-3-Gutenberg` (contextual search with 3 lines of surrounding context)

![find -type f -size 94c -exec ls -lh search result frankenstein.txt](./images/05-find-size-search.png)

`find ./1b-3-Gutenberg -type f -size 94c -exec ls -lh {} \;` → frankenstein.txt (Size based search)

![find -type f -printf date and path sorted output](./images/06-find-date-search.png)

`find ./1b-3-Gutenberg -type f -printf '%T+ %p\n' | sort` (Date based search)

![du -a sort -nr head showing largest file size](./images/07-du-largest-file.png)

Using `du -a` to search for the largest file size

![sed word frequency analysis on frankenstein.txt](./images/08-sed-word-frequency.png)

Word frequency analysis on Frankenstein.txt — using `sed` to split the text into one word per line and sort to count and rank each word by frequency
