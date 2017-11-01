# Shodan Parser

Shodan Parser will parse JSON data exported from SHODAN and create IP:PORT formatted
list to be used with other tools. To run specify path to a file with JSON
data from SHODAN.

## Requirements

```pip install click```

## Usage and options

```
Usage: shodan-parser.py [OPTIONS] SHODAN_JSON_FILE

  This script will parse JSON data from SHODAN and create IP:PORT formatted
  list to be used with other tools. To run specify path to a file with JSON
  data from SHODAN.

Options:
  --version                Show the version and exit.
  -o, --output TEXT        Path to output file with parsed data. IP:PORT
                           format, one entry per line  [default: targets.txt]
  -v, --verbose            Verbose mode  [default: False]
  -n, --log-every INTEGER  Show log after specified number of entries parsed.
                           Effective only in verbose mode  [default: 100]
  -h, --help               Show this message and exit.
```

#### Examples

```python shodan-parser.py shodan_data.json```

```python shodan-parser.py -o custom_output.txt -v shodan_data.json```

```python shodan-parser.py -o custom_output.txt -v -n 10 shodan_data.json```