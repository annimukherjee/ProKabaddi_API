| <img width="200" alt="kabaddi_api_logo" src="https://github.com/user-attachments/assets/e074c4c2-18b3-4580-a9dd-1aa40f9495b0"> | <h2>ProKabaddi API - Data collection and analysis tools for professional Kabaddi leagues</h3><p align="center"><a href="#features">Features</a> • <a href="#installation">Installation</a> • <a href="#usage">Usage</a> • <a href="#contributing">Contributing</a> • <a href="#license">License</a> • <a href="https://annimukherjee.github.io/ProKabaddi_API/">Documentation</a></p> |
|:---:|:---|


# Moved to: https://github.com/kabaddiPy/kabaddiPy

---

Kabaddi Data Aggregator is a Python module that provides tools for collecting and analyzing data from professional Kabaddi leagues. It uses web scraping techniques to gather information about teams, players, and match statistics from various online sources.

## Installation 

Please install the development version of `ProKabaddi_API` using pip:


```shell
pip install pro_kabaddi_data
```

Deployed here: https://pypi.org/project/pro-kabaddi-data/

## Requirements

- Python 3.7+
- Selenium WebDriver
- Firefox browser (for Selenium WebDriver)
- BeautifulSoup4


## Usage

Here's a quick minimal example of how to get started with the Kabaddi Data Aggregator:

```python
from prokabaddidata import prokabaddidata

# Initialize the aggregator
aggregator = prokabaddidata.KabaddiDataAggregator()

# Get all player information for a specific team
players_info = aggregator.player_performance(team="Patna Pirates")

```

For more detailed usage instructions and API documentation, please refer to our [documentation page](https://annimukherjee.github.io/ProKabaddi_API/).

## Features
Here are our current features. New and better features are actively being developed!!

### Current season standings

```python
standings = aggregator.team_season_standings(team=None, rank=None)
```
Return the current season rankings of all teams by default
#### **Parameters**
- team (str, optional): Get season rank by team name
- rank (int, optional): Get team by season rank

### Player Performance
```python
stats = aggregator.player_performance("team="Bengal Warriors")
```
Returns career level player metrics. `team` should be specified.

### Loading Lifetime Data

```python
player_df = aggregator.load_data(PlayerDetails=True, TeamDetails = False, TeamMembers = False)
```
Defaults to loading lifetime player data for all teams.
#### **Parameters**
- PlayerDetails (bool): Loads player details into a DataFrame. Default is `True`.
- TeamDetails (bool): Loads team-level statistics into a DataFrame. Default is `False`.
- TeamMembers (bool): Loads the details of current team members into a DataFrame. Default is `False`.

### Team level stats
```python
teamstats = aggregator.team_level_stats(season=None)
```
Returns team-level stats by season. Defaults to latest season.

## Contributing

We welcome contributions to the Kabaddi Data Aggregator project! If you'd like to contribute, please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin feature/your-feature-name`)
6. Create a new Pull Request



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the various website owners for providing the data sources

## Contact

If you have any questions, feel free to reach out to [Aniruddha Mukherjee] at [mukh.aniruddha@gmail.com] or open an issue in the GitHub repository.

---

<p align="center">
  Made with ❤️ for Kabaddi enthusiasts and data analysts
</p>

Please star this repository if you found it helpful! Your support is greatly appreciated.
