# Weedmaps Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [Weedmaps Scraper](https://oxylabs.io/products/scraper-api/ecommerce/weedmaps?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Weedmaps website effortlessly. This brief guide explains how an Weedmaps Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Weedmaps results by providing your own URLs to our service. We can return the HTML for any Weedmaps page you like.

#### Python code example

The example below illustrates how you can get HTML of Weedmaps page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://weedmaps.com/brands'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/weedmaps-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta name=\"viewport\" content=\"initial-scale=1.0, width=device- ... </html>",
      "created_at": "2023-12-18 11:19:19",
      "updated_at": "2023-12-18 11:19:33",
      "page": 1,
      "url": "https://weedmaps.com/brands",
      "job_id": "7142473401330886657",
      "status_code": 200
    }
  ]
}
```
With our Weedmaps Scraper, you can seamlessly pull public data from any Weedmaps web page. Gather the invaluable shop information you need, like location, available strains, or shop ratings, to fully understand the market and get an edge on your competitors. If you have any quandaries or require assistance, feel free to reach out to our devoted support team via live chat or shoot us an email at hello@oxylabs.io.
