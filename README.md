# Worten Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Worten Scraper](https://oxylabs.io/products/scraper-api/ecommerce/worten?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Worten website effortlessly. This brief guide showcases how Worten Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Worten results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Worten page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.worten.pt/promocoes/pequenos-eletrodomesticos'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/worten-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"pt-PT\" data-capo=\"\"><head><meta charset=\"utf-8\">\n<meta name=\"viewport\" co ... </html>",
      "created_at": "2024-02-20 12:42:22",
      "updated_at": "2024-02-20 12:42:24",
      "page": 1,
      "url": "https://www.worten.pt/promocoes/pequenos-eletrodomesticos",
      "job_id": "7165687125755597825",
      "status_code": 200
    }
  ]
}
```
Using our special Worten Scraper, you can conveniently pull out public data from any desired Worten web page. Gather all pertinent product data, such as the trending appliances, updated gadget details, or the opinions of tech enthusiasts to better understand the market dynamics and outmaneuver your rivals. In case of any queries, reach out to our dedicated support team through live chat or send them an email at hello@oxylabs.io.
