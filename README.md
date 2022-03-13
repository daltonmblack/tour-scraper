# tour-scraper
Web scraper that aggregates tour dates in desired cities

## Initial Setup

### Basic Project Setup

* Validate that Python 3.8 is installed via `python -V`
  * If you have both Python 2 and Python 3 installed, you will need to use `python3` in place of `python` in the commands below
  * If Python 3.8 isn't installed anywhere on your system, one option is to install it using `pyenv`: https://realpython.com/intro-to-pyenv/
* Install `pipenv`:
```bash
python -m pip install --user pipenv
```
* Install the packages required for this project
```
pipenv install
```
* Create a `.env` file in the root directory of this project
  * This will be used to store environment-specific values. More details will be explained below.

### Install `ChromeDriver`

* Find your current Chrome version at: chrome://settings/help
  * For example: `Version 99.0.4844.51 (Official Build) (64-bit)`
* Download the `ChromeDriver` which corresponds to the Chrome version above from: https://chromedriver.chromium.org/downloads
  * Store the downloaded binary somewhere you'll remember
* Add an entry to your `.env` file containing the path to the `ChromeDriver` binary
```
WEBDRIVER_PATH=<path_to_chrome_driver_binary>
```


## Running Tour Scraper

```bash
pipenv run python tour_scraper.py
```
