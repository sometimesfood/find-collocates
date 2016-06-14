# find-collocates

A primitive collocate extractor using NLTK.

## Dependencies

Python 2.7 and NLTK. On Debian Jessie, these can be installed using
`apt-get`:

   sudo apt-get install python-nltk python-unicodecsv

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
