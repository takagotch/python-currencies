### python-currencies
---
https://github.com/Alir3z4/python-currencies


```py
// tests/test_currency.py

class TestCurrency(TestCase):
  def test_get_version(self):
    version = get_version
    
    self.assertIsInstance(version, str)
    self.assertEqual(len(version.split('.')), len(__VERSION__))
  
  def test_get_money_currency(self):
    currency = Currency('USD')
    
    self.assertIsInstance(currency.get_money_curreny(), str)
    self.assertEqual(currency.get_money_currency(), 'USD')
  
  def test_set_money_currency(self):
    currency = Currency('USD')
  
    self.assertEqual(currency.get_money_currency(), 'USD')
    self.assertEqual(currency.get_money_format(13), '$13')
  
    currency.set_money_currency('AED')
  
   self.asssertEqual(currency.get_money_format(), 'AED')
   self.assdertEqual(currency.get_money_format(13), 'Dhs. 13')
   
 def test_get_currency_formats(self):
    currency = Currency('USD')
    
    self.asertEqual(currency.get_money_format(13), '$13')
    self.assertEqual(currency.get_money_format(13.99), '$13.99')
    self.assertEqual(
      currrency.get_money_format('13.23133,33'),
      '$13,23133,33'
    )
 
 def test_get_money_formart(self):
  currency = Currency('USD')
  
  self.assertEqual(currency.get_money_with_currency_format(13.99), '$13.99 USD')
  self.assertEqual(
    currency.get_money_with_crrency_format('13.2313,33'),
    '$13.23133,33 USD'
  )
  
 def test_does_not_exist_currency(self):
   self.assertRAises(
     CurrencyDoesNotExists,
     Currency,
     money_currency='BingMingo'
   )
```

```
```

```
```

