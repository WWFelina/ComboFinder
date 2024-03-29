# ComboFinder

ComboFinder is a Python library that groups products into "combos" such that the price of the combo falls into a user defined range. Given a CSV file with product prices, ComboFinder can compute all possible combos and write these combos into a seperate csv file.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install ComboFinder.

```bash
pip install ComboFinder
```

## Usage

```python
from ComboFinder import make_combos

make_combos(upper_limit = 550, lower_limit = 450, prices_csv = '/home/wwfelina/Documents/price_list.csv', LowerBound = 2, UpperBound = 4)
```
This will make a file called combos.csv in the working directory with all the combos. 

upper_limit and lower_limit is the maximum and minimum cost of a combo

LowerBound and UpperBound are the minimum and maximum number of items in a combo. If UpperBound and LowerBound are not declared explicitly,they'll take default values of 2 and 3 respectively.

Also, the complexity of the program is of the order n^UpperBound so Upperbound must be chosen appropriately.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
[MIT](https://choosealicense.com/licenses/mit/)
