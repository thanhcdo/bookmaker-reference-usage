# bookmaker-reference-usage

Python script that reads sports data from local CSV files, analyzes it, and updates a SharePoint Excel file with the results.

## How it works

1. **Extract**: read the local CSV files, one file per sport.
2. **Analyze**: process the data and compute the reference usage figures.
3. **Update**: write the results to the SharePoint Excel file.

## Requirements

- Python 3.10 or newer
- Dependencies listed in `requirements.txt`
- Access to the target SharePoint Excel file

## Installation

```bash
git clone https://github.com/<owner>/bookmaker-reference-usage.git
cd bookmaker-reference-usage
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Input data

Place the CSV files in the data folder (path configurable, see below). Each file contains the data for one sport:

```
data/
├── soccer.csv
├── basketball.csv
├── ice-hockey.csv
├── tennis.csv
└── rugby.csv
```

Describe the expected columns here.

## Usage

```bash
python main.py
```

Describe any command-line options here.

## Configuration

| Option | Description |
| ------ | ----------- |
| Data folder | Location of the CSV files |
| SharePoint file | Target Excel file to update |
| Credentials | How authentication to SharePoint is provided |

## Output

Describe which sheets, tables, or ranges in the SharePoint Excel file are updated, and whether existing data is replaced or appended.

## Troubleshooting

- **Missing CSV file:** check that the file for the sport exists in the data folder.
- **SharePoint update fails:** check your credentials and that the Excel file is not locked by another user.

## License

This project is distributed under an End User License Agreement (EULA). Use, copying, and redistribution are governed by its terms.
