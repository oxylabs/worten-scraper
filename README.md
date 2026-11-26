# Worten Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=github&utm_medium=referral&utm_content=worten-scraper&utm_campaign=banner&groupid=877)

<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

Oxylabs' [Worten Scraper](https://oxylabs.io/products/scraper-api/ecommerce/worten?utm_source=github&utm_medium=referral&utm_content=worten-scraper&groupid=877) is a data gathering solution allowing you to extract real-time information from an Worten website effortlessly. This brief guide showcases how Worten Scraper works, along with code examples to help you better understand how to use it hassle-free.

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
      "created_at": "2025-02-20 12:42:22",
      "updated_at": "2025-02-20 12:42:24",
      "page": 1,
      "url": "https://www.worten.pt/promocoes/pequenos-eletrodomesticos",
      "job_id": "7165687125755597825",
      "status_code": 200
    }
  ]
}
```
Using our special Worten Scraper, you can conveniently pull out public data from any desired Worten web page. Gather all pertinent product data, such as the trending appliances, updated gadget details, or the opinions of tech enthusiasts to better understand the market dynamics and outmaneuver your rivals. In case of any queries, reach out to our dedicated support team through live chat or send them an email at hello@oxylabs.io.
