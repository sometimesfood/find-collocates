# find-collocates

A primitive collocate extractor using NLTK.

## Dependencies

Python 2.7 and NLTK. On Debian Jessie, these can be installed using
`apt-get`:

   sudo apt-get install python-nltk python-unicodecsv

## Usage example

Find collocates of the word "bryllyg":

```bash
./find-collocates \
  --cutoff-frequency 15 \
  --select-word bryllyg \
  --number-of-results 2000 \
  ~/corpus-directory/ > collocates.csv
```
