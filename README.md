# Web Price Watcher

A tiny script that scrapes a page in headless Chrome and sends an ntfy.sh notification when your target text (a price) changes. Currently, the example is checking Palworld's price on Steam, but you can easily adapt it to other websites by changing the URL and CSS selectors. It scrapes the pages every 24 hours, but you can change the schedule as needed. Scrape data is saved to a JSON file, so it can be compared with the last scraped data.

> Based on: [slashtechno/scrape-and-ntfy](https://github.com/slashtechno/scrape-and-ntfy/tree/main) The Ntfy class was adapted from there.

## Install

```bash
git clone https://github.com/Bai756/website-price-notifier.git
cd web-price-watcher
pip install selenium webdriver-manager httpx schedule
```

## Usage

To use, edit the top of the main function. Add your own urls and css-selectors, and change the ntfy_notifier url to your ntfy topic. Add as many `PriceScraper` instances as you want.

Then run:

```bash
python main.py
```
