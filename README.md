# Tour Scraper
Web scraper that aggregates tour dates in desired cities

## Initial Setup

### Basic Project Setup

* Validate that Python 3.8 is installed (e.g., `python -V`)
  * If you have both Python 2 and Python 3 installed, you will need to use `python3` in place of `python` in the commands below
  * If Python 3.8 isn't installed anywhere on your system, one option is to install it using `pyenv`: https://realpython.com/intro-to-pyenv/
* Install `pipenv` which is used to install the packages for this project:
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

* Find your current Chrome version at: [chrome://settings/help](chrome://settings/help)
  * For example: `Version 99.0.4844.51 (Official Build) (64-bit)`
  * The only portion of the version that matters is the first value. I.e., `99` in the version above.
* Download the `ChromeDriver` which corresponds to the Chrome version above from: https://chromedriver.chromium.org/downloads
  * Store the downloaded binary somewhere you'll remember
* Manually run the binary (e.g., double click) and enable any necessary permissions for the binary to be run
  * On Mac OSX, you may need to navigate to `System Preferences` -> `Security and Privacy` -> `General` -> unlock the lock on the bottom-left -> click `Open anyway` on the prompt in the bottom-right which is talking about `chromedriver`
  * On Windows: TODO
* Close the manually run `chromedriver` process
* Add an entry to your `.env` file containing the path to the `ChromeDriver` binary
```
WEBDRIVER_PATH=<path_to_chrome_driver_binary>
```


## Running Tour Scraper

The current version of this project only searches for concerts from the band [Jinjer](http://jinjer-metal.com/).

```
pipenv run python tour_scraper.py --state=<us_state>
```

To see the full set of program options, run:
```
pipenv run python tour_scraper.py --help
```
