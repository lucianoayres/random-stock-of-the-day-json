## Random Stock of the Day JSON

**Random Stock of the Day JSON** provides a daily random stock ticker from the Brazilian stock exchange (B3) in JSON format.

### Description

Each day, this repository features a JSON file named `b3-ticker.json` containing a random stock ticker from the B3 stock exchange. The format of the JSON file is as follows:

```json
{
    "ticker": "PETR",
    "name": "PETROBRAS"
}
```

Additionally, a file named `b3-last-picks.json` keeps track of all the randomly picked stock tickers. This file logs each ticker that has been selected until all items from the original source have been picked, at which point the cycle starts over.

The stock ticker is updated daily by a scheduled GitHub Actions workflow that runs at 2:47 AM UTC. The workflow fetches data from the [Brazil Stocks Tickers JSON](https://github.com/lucianoayres/brazil-stocks-tickers-json) repository, which provides an extensive list of B3 stocks.

### Usage

-   **`b3-ticker.json`**: Contains the current random stock ticker for the day.
-   **`b3-last-picks.json`**: Logs all previously picked stock tickers to ensure that each stock is picked once before the cycle resets.

To view the current random stock ticker, check the `b3-ticker.json` file. The `b3-last-picks.json` file provides a history of the stocks that have been picked.

### Contributions

Feel free to contribute by suggesting improvements or reporting issues. Pull requests are welcome!

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
