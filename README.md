# find-collocates

A primitive collocate extractor using NLTK.

## Dependencies

Python 3.9 and NLTK. On Debian Bullseye, these can be installed using
`apt`:

   sudo apt install python3-nltk

## Getting started

No installation needed. Simply clone the git repo to a local directory
and start using the script.

## Usage example
Find collocates of the word "bryllyg":

```bash
./find-collocates \
  --cutoff-frequency 15 \
  --select-word bryllyg \
  --number-of-results 2000 \
  ~/corpus-directory/ > collocates.csv
```

Find collocates of all the words in `input.txt` (one word per line):

```bash
while read word; do
./find-collocates \
  --cutoff-frequency 15 \
  --select-word ${word} \
  ~/corpus-directory/ > "collocates-${word}.csv"
done < input.txt
```
