# Description
This Python script downloads hospital-related datasets from the CMS provider data API. It filters datasets by the theme "hospital," downloads the CSV files, converts column headers to snake_case, and saves them locally in a `data` directory. The script uses multithreading to speed up downloads.

#Features
- Fetches datasets from CMS API
- Filters datasets with "hospital" in their theme
- Downloads CSV files and cleans column names
- Saves processed files in a local folder
- Uses ThreadPoolExecutor for parallel downloads

# Requirements
- Python 3.7 or higher
- `requests` library
- `pandas` library

# Installation
Install dependencies using pip:

```bash
pip install requests pandas
Usage
Run the script:

bashpython your_script_name.py
Downloaded CSV files will be saved in the data folder.

Functions
snake_case(name): Converts strings to snake_case format.
load_last_run(): Loads the timestamp of the last run (not currently used).
save_last_run(timestamp): Saves the timestamp of the last run (not currently used).
get_datasets(): Fetches and filters hospital datasets from the API.
download_dataset(dataset): Downloads and processes a single dataset CSV.
main(): Coordinates dataset fetching and parallel downloading.

Notes
The script downloads all hospital datasets every time it runs.
You can modify it to support incremental downloads using last run timestamps.
Ensure you have internet access to download datasets.
