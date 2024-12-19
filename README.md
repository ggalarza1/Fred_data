# Fred_data
The Federal Reserve Economic Data (FRED) API is very useful to fetch different economic data.

First you need to create an account.
Go to https://fredaccount.stlouisfed.org/ .
Create an account. Click on my account. On the left hand side you will find API. 
Click on the +Request API Key and copy the API Key. 
You can now use this to pull data from the API.

# Installation 
```
pip install fredapi
```

# API Key Environment
```
from fredapi import Fred
fred = Fred(api_key = 'your api key')

#You need to insert the api key above. Once you do that, you can start using the API.

data = fred.get_series_latest_release('GDP')
data.tail()
```

# Navigating the Fred API

Per Fred API documentation,

you can search the data by categories. You must specify which category you want to go to.

```
fred.search_by_category(category_id=16)
```
You can search the data by release. You must specify which release you want to investigate.

```
fred.search_by_release(release_id=188)
```

You can also search by series. You must specify which series you want to explore.

```
fred.search('bea')
```

There's probably more but these were the only ones I investigated on this notebook.
