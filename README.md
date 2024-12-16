# Fred_data
The Federal Reserve Economic Data (FRED) API is very useful to fetch different economic data.

First you need to create an account.
Go to https://fredaccount.stlouisfed.org/
Click on my account. On the left hand side you will find API. 
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
