# bsc-tokenwatch
Python script that scrapes new Bsc tokens from Poocoin and checks if they are rugpulls and honeypots and stores the data in a excel file
Installation
---
Preferably, you can download sqlmap by cloning the Git repository:
  ```bash
  git clone https://github.com/theinit01/bsc-tokenwatch
  ```
Download all the requirements from the requirements.txt
  ```python
  pip install -r requirements.txt
  ```
How it does the stuff:
---
This script uses selenium, python web driver to automate browser to go to poocoin.app/ape and scape the data using BeautifulSoup. Since all the sites used int his script, i.e, poocoin and bscscan, blocks pyhton requests module to get the data and source code, Browser automation is the only way left for using the script.
Script scraps the new tokens on poocoin.app/ape and check for rugpulls, like checking if the top holder of the coin is a Burn Address or a Liquidity Pool and then checking if the liquity pool has most stuff burned or locked in a contract
 ```
 Disclaimer: All the data classified as non-rugpulls and honeypots are detected by this bot, which maybe true or false.
 The developer is not responsible and liable for any wrong data detected by the bot.
 Please do your own research before buying anything. 
```
What you need to do to get started
---
1. Download any selenium browser webdriver, but chromedriver is preferred. Download from [here](https://chromedriver.chromium.org/downloads)
2. Add the path to the chromedriver in the script main.py at the line number 14. 
3. You can use options like using chrome in headless mode by uncommenting the line 19.
4. The script adds excel files in the excel folder by date sort. If using many times in a day, the script adds different sheets in a file by the name of the time at which it is started
5. If your Internet Connection is slow or you are getting any error, try increasing time in seconds in the sleep command in line 34, 106, 167, 179, 229. and try running the script again and again

