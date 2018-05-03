# PyYaraScanner

A simple many-rules to many-files YARA scanner for incident response or malware zoos.
## Prerequisites

Python 2.7 with the Yara-Python package

``` 
pip install yara-python
```

## Running a scan

To run with default settings, just specify a folder for .yar rules and a starting point for files to scan. All directories for both inputs are scanned recursively.

```
pyarascanner.py Yara_Rules C:\
```
Full syntax:

```
pyarascanner.py [-h] [-e] [-a] [-l LOG] [-m MAXSIZE] rules_path scan_path
```

### Optional Arguments

* -h, --help            Show help
* -e, --errors          Show all errors
* -a, --alerts          Show alerts only
* -l LOG, --log LOG     Output to specified log file
* -m MAXSIZE, --maxsize MAXSIZE
                        Set maximum file size (MB)

## Built With

* [Yara-Python](https://github.com/VirusTotal/yara-python) - The awesome python implementation of awesome YARA rules