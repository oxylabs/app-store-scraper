# App Store Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [App Store Scraper](https://oxylabs.io/products/scraper-api/web/app-store-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any App Store effortlessly. This brief guide explains how an App Store Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get App Store results by providing your own URLs to our service. We can return the HTML for any App Store page you like.

#### Python code example

The example below illustrates how you can get [apple.com](https://www.apple.com/app-store/) App Store HTML results.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.apple.com/app-store/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/app-store-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html class=\"no-js\" xmlns=\"http://www.w3.org/1999/xhtml\" xml:lang=\"en-US\" lang=\"en-U ... </html>",
      "created_at": "2023-12-18 11:35:39",
      "updated_at": "2023-12-18 11:35:41",
      "page": 1,
      "url": "https://www.apple.com/app-store/",
      "job_id": "7142477513275482113",
      "status_code": 200
    }
  ]
}
```
With our App Store Scraper, you can seamlessly extract public data from any App Store web page. Gather crucial app data such as app ratings, developer details, update history, and the number of downloads to gain insights into market trends and outperform your rivals. If you have any queries, feel free to reach out to our support team via live chat or shoot us an email at hello@oxylabs.io.
