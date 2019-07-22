# Open BNM API

[![PyPi Downloads](https://pepy.tech/badge/openbnmapi)](https://pepy.tech/project/openbnmapi)
[![PyPI version](https://badge.fury.io/py/openbnmapi.svg)](https://badge.fury.io/py/openbnmapi)

This is an unofficial Python wrapper for the Bank Negara Malaysia Open API. (https://api.bnm.gov.my/portal)

### Installation

Using pip:
```
pip install openbnmapi
```
### Example Usage
```python
import openbnmapi

obnmapi = OpenBNMAPI()

# Get latest Base Rates and Base Lending Rates
br = obnmapi.base_rate()
print(br)
```
### Currently supports the following endpoints:
- Base Rates/BLR (https://api.bnm.gov.my/portal#tag/Base-RatesBLREffective-LR)
  - Latest Base Rate
  ```python
  obnmapi.base_rate()
  ```
  - Latest Base_rate by bank code
    - 'bank_code' accepts 8 characters of SWIFT code
  ```python
  obnmapi.base_rate(bank_code="BKKBMYKL")
  ```
- Daily FX Turnover (https://api.bnm.gov.my/portal#tag/Daily-FX-Turnover)
  - Latest Daily FX Turnover
  ```python
  obnmapi.daily_fx_turnover()
  ```
- Exchange Rates
- Financial Consumer Alert
  - Latest List of Financial Consumer Alert
   ```python
  obnmapi.consumer_alert()
  ```
- Interbank Swap
- Interest Rate
- Interest Volume
- Islamic Interbank Rate
- Kijang Emas
- Overnight Policy Rate (OPR)
- Renminbi
- USD/MYR Interbank Intraday Rate
- Kuala Lumpur USD/MYR Reference Rate

### To - Do
Implement 
- Finish Documentation including input parameters and return values
- More proper error handling
- Add Request Time Out handling
- Cache mechanism 
- Pandas dataframe support

