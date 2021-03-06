# BlackFortPay

BlackFort Payment API client for Python 3.6+

## Installation

`pip install blackfortpay`

## Usage

```python
from blackfortpay import BlackFortPaymentAPI

# pass API User key and API Secret key or store them as environment variables BLACKFORT_API_USER_KEY and BLACKFORT_API_SECRET_KEY
>>> client = BlackFortPaymentAPI('api-user', 'api-secret')  # also you can pass pos_id and locale
>>> rate = client.start_payment(invoice_amount=100, invoice_currency='EUR', currency='BTC')
GetRateResponse(invoice_currency='EUR', invoice_amount='100.00', currency='BTC', rate='7014.0000', amount_exchange='0.01425719', network_processing_fee='0.00000452', amount='0.01425945', wait_time='7 minutes', fast_transaction_fee='0.00033656', fast_transaction_fee_currency='BTC/kB', payment_id='2a1eb341-5e87-4ad8-9f0b-089f5ff027f6')
>>> rate.rate
'7014.0000'
# Change pos_id and locale if needed by set_pos_id() and set_locale() methods
```

API reference available [here](https://pay.blackfort.exchange/payInfo.api)
