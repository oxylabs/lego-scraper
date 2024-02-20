# Lego Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Lego Scraper](https://oxylabs.io/products/scraper-api/ecommerce/lego?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Lego website effortlessly. This brief guide showcases how Lego Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Lego results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Lego page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.lego.com/en-us/bestsellers'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/lego-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width=dev ... </html>",
      "created_at": "2024-02-20 12:36:18",
      "updated_at": "2024-02-20 12:36:20",
      "page": 1,
      "url": "https://www.lego.com/en-us/bestsellers",
      "job_id": "7165685598034866177",
      "status_code": 200
    }
  ]
}
```
With our Lego Scraper, you can seamlessly extract public data from any Lego web page. Gather important product information, such as set dimensions, brick counts, or set themes, to understand Lego trends and keep ahead of your competitors. If you require assistance, reach out to our support team via live chat or email us at hello@oxylabs.io.